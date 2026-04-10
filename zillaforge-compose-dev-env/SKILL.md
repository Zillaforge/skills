---
name: docker-compose-dev-env
description: 'Generate a devcontainer + docker-compose development environment for any project using a 3-layer architecture (persistent/system/service). Use when: scaffolding docker-compose dev environment, creating devcontainer configuration, adding Makefile dev targets, setting up infrastructure services (DB, MQ, cache), enabling profile-based service toggling, or reproducing the pegasus-cloud docker-compose pattern in a new project.'
argument-hint: 'Describe the project, its dependencies (DB, MQ, cache, etc.), and which services need containers'
---

# Devcontainer + Docker-Compose Development Environment Generator

## When to Use
- Scaffolding a new project's `docker-compose/` dev environment from scratch
- Adding devcontainer support with Docker-outside-of-Docker to an existing project
- Creating Makefile targets for managing a multi-container dev environment
- Setting up infrastructure (database, message queue, cache) as containers for local development
- Generating profile-based `.env` files to toggle services on/off

## Architecture Pattern

This skill generates a **3-layer docker-compose architecture** with a devcontainer that can run the main application locally while all dependencies run as containers.

```
┌───────────────────────────────────────────────────────────────┐
│  Layer 0: Devcontainer                                        │
│  ├── Application runs locally (go run / debug / make start)   │
│  ├── Uses config files from docker-compose/etc/               │
│  ├── Docker-outside-of-Docker (controls host Docker)          │
│  └── HOST_PROJECT_PATH remoteEnv for volume mount resolution  │
├───────────────────────────────────────────────────────────────┤
│  Layer 1: service/ — Application services                     │
│  ├── Each service has TWO profiles: dev (build from source)   │
│  │   and release (pre-built image)                            │
│  ├── Controlled by .env profile variables (*_DISABLE=true)    │
│  └── docker-compose project: "<prefix>-service"               │
├───────────────────────────────────────────────────────────────┤
│  Layer 2: system/ — Infrastructure services                   │
│  ├── Always-on: DB, MQ, Cache (required)                      │
│  ├── Optional: Swagger UI, admin tools, tracing (profiles)    │
│  ├── ONE yaml file per service (independent lifecycle)        │
│  └── docker-compose project: "<prefix>-system"                │
├───────────────────────────────────────────────────────────────┤
│  Layer 3: persistent/ — Networks and Volumes                  │
│  ├── Shared bridge network with fixed subnet                  │
│  ├── Named volumes for data persistence                       │
│  ├── Created with --no-start (volumes/networks only)          │
│  └── docker-compose project: "<prefix>-system" (same)         │
└───────────────────────────────────────────────────────────────┘
```

**Key design principles:**
- Each service gets its own `docker-compose.*.yaml` file — start/stop independently
- All containers share one external bridge network with fixed IPs
- Volumes declared as external, created by persistent layer
- Profile-based toggling via `.env` variables — `*_DISABLE=true` disables, comment out to enable
- Source-build and release-image variants for each service
- Makefile wildcards iterate all yaml files per layer

## Procedure

### Step 1: Gather Project Requirements

Ask the user for:

1. **Project language & framework** (Go, Node.js, Python, Java, etc.)
2. **Infrastructure dependencies:**
   - Database: MariaDB/MySQL, PostgreSQL, MongoDB, etc.
   - Message Queue: RabbitMQ, Kafka, NATS, etc.
   - Cache: Redis (standalone or sentinel), Memcached, etc.
   - Other: Docker-in-Docker, object storage, registry, etc.
3. **Application services** the project depends on (e.g., IAM server, API gateway, other microservices)
4. **Project name and abbreviation** (used as docker-compose project prefix, container name prefix)
5. **Network subnet** to use (default: `172.40.0.0/16`)
6. **Config files** the application needs at runtime

### Step 2: Generate Directory Structure

Create the following structure under the project root:

```
<project>/
├── .devcontainer/
│   ├── Dockerfile
│   └── devcontainer.json
├── docker-compose/
│   ├── README.md
│   ├── etc/                              # Runtime config files
│   │   ├── <app>.yaml                    # Main app config
│   │   └── <dependency>.yaml             # Dependency configs
│   ├── persistent/                       # Networks + Volumes
│   │   ├── docker-compose.network.yaml
│   │   ├── docker-compose.volume.<name>.yaml
│   │   └── ...
│   ├── service/                          # Application services
│   │   ├── .env                          # Profile toggles
│   │   ├── docker-compose.<svc>.yaml
│   │   └── ...
│   └── system/                           # Infrastructure
│       ├── .env                          # Optional service toggles
│       ├── docker-compose.<infra>.yaml
│       └── ...
└── Makefile                              # Dev targets (add/merge)
```

### Step 3: Generate Persistent Layer

#### 3a. Network file

Create `docker-compose/persistent/docker-compose.network.yaml`:

```yaml
services:
  <prefix>-network:
    container_name: network
    image: alpine:3.20                      # Lightweight placeholder
    networks:
      <prefix>-network:
        ipv4_address: <subnet>.0.2

networks:
  <prefix>-network:
    name: <prefix>-network
    driver: bridge
    ipam:
      driver: default
      config:
        - subnet: <subnet>.0.0/16
          gateway: <subnet>.0.1
```

#### 3b. Volume files

Create one `docker-compose.volume.<name>.yaml` per named volume:

```yaml
services:
  <prefix>-<volume-purpose>:
    container_name: <volume-purpose>
    image: alpine:3.20
    volumes:
      - <prefix>-<volume-name>:/mnt
    networks:
      <prefix>-network:
        ipv4_address: <subnet>.0.<N>

networks:
  <prefix>-network:
    external: true
    name: <prefix>-network

volumes:
  <prefix>-<volume-name>:
    name: <prefix>-<volume-name>
```

### Step 4: Generate System Layer

Create one file per infrastructure service under `docker-compose/system/`.

#### Pattern for always-on service:

```yaml
services:
  <prefix>-<service>:
    image: <official-image>:<version>
    container_name: <service-name>
    environment:
      - <ENV_VARS>
    networks:
      <prefix>-network:
        ipv4_address: <subnet>.<group>.<N>
    volumes:
      - <prefix>-<service>-data:/var/lib/<data-path>
    ports:
      - "<host-port>:<container-port>"

networks:
  <prefix>-network:
    external: true
    name: <prefix>-network

volumes:
  <prefix>-<service>-data:
    external: true
    name: <prefix>-<service>-data
```

#### Pattern for optional service (profile-controlled):

```yaml
services:
  <prefix>-<service>:
    profiles:
      - ${<SERVICE>_DISABLE:-}         # When variable is set → disabled
    image: <image>
    container_name: <service-name>
    networks:
      <prefix>-network:
        ipv4_address: <subnet>.<group>.<N>
    ports:
      - "<host-port>:<container-port>"

networks:
  <prefix>-network:
    external: true
    name: <prefix>-network
```

#### System `.env` file:

```env
SWAGGER_DISABLE=true        # comment to enable
PHPMYADMIN_DISABLE=true     # comment to enable
# Add more optional services...
```

**IP allocation convention:**
- `<subnet>.0.x` — persistent/network utilities
- `<subnet>.100.x` — application services (group 1)
- `<subnet>.115.x` — application services (group 2)
- `<subnet>.200.x` — databases
- `<subnet>.201.x` — message queues
- `<subnet>.202.x` — cache
- `<subnet>.203+` — other infrastructure

### Step 5: Generate Service Layer

Each application service gets **two profiles** in one YAML file: dev (build from source) and release (pre-built image).

#### Pattern:

```yaml
services:
  # Dev profile: builds from source, mounts source code
  <prefix>-<service>:
    profiles:
      - ${<SERVICE>_DISABLE:-}
    image: <build-image>                    # e.g., golang:1.22.4-alpine
    container_name: <service-name>
    networks:
      <prefix>-network:
        ipv4_address: <subnet>.<group>.<N>
    working_dir: /home/${<SERVICE>_FOLDER_NAME}
    environment:
      - GOPROXY=${GOPROXY}
    volumes:
      - ${PWD}/..:/home                     # Mount parent dir (multi-repo)
      - ${PWD}/docker-compose/etc/<cfg>:/mnt/<cfg>
    entrypoint:
      - "sh"
      - "-c"
      - |-
        <install-build-deps> && \
        <build-command> && \
        <run-command>
    ports:
      - "<host-port>:<container-port>"

  # Release profile: uses pre-built image
  <prefix>-<service>-release:
    profiles:
      - ${<SERVICE>_RELEASE_DISABLE:-}
    image: <registry>/<image>:<version>
    container_name: <service-name>-release
    networks:
      <prefix>-network:
        ipv4_address: <subnet>.<group>.<N+1>
    volumes:
      - ${PWD}/docker-compose/etc/<cfg>:/mnt/<cfg>
    command: [<run-args>]
    ports:
      - "<host-port>:<container-port>"
    restart: on-failure

networks:
  <prefix>-network:
    external: true
    name: <prefix>-network

volumes:
  # Declare all needed external volumes
  <prefix>-<vol-name>:
    name: <prefix>-<vol-name>
    external: true
```

#### Service `.env` file:

```env
GOPROXY="https://proxy.golang.org"

<SERVICE>_FOLDER_NAME=<repo-directory-name>

# For each service, two lines:
<SERVICE>_DISABLE=true             # comment to enable dev (source build)
# <SERVICE>_RELEASE_DISABLE=true   # comment to enable release image
```

**Convention:** By default, disable ALL services. The developer enables only what they need. The service they are actively developing stays disabled and runs locally via `make start` or debugger.

### Step 6: Generate Config Files

Place application runtime config files in `docker-compose/etc/`. These should reference infrastructure services by **container name** (DNS via shared network):

```yaml
# Example: database config referencing MariaDB container
storage:
  provider: mariadb
  mariadb:
    host: <prefix>-mariadb:3306         # Use container name, not localhost
    account: root
    password: <password>
    name: <db-name>

# Example: message queue referencing RabbitMQ container
message_queue:
  provider: rabbitmq
  rabbitmq:
    host: <prefix>-rabbitmq:5672
    account: guest
    password: guest

# Example: cache referencing Redis container
cache:
  service: my_redis_sentinel
services:
  - name: my_redis_sentinel
    kind: redis_sentinel
    hosts:
      - <prefix>-redis-sentinel:26379
    password: <password>
    sentinel_password: <sentinel-password>
    master_group_name: mymaster
```

### Step 7: Generate Makefile Targets

Add (or merge) the following targets to the project's `Makefile`:

```makefile
# --- Path handling for devcontainer ---
LOCAL_PWD := $(shell pwd)
HOST_PWD := $(or $(HOST_PROJECT_PATH),$(LOCAL_PWD))
ARCH ?= $(shell uname -m | sed 's/x86_64/amd64/' | sed 's/aarch64/arm64/')

# --- Run application locally (dev mode) ---
.PHONY: start
start:
	@<run-command-with-config-from-docker-compose/etc/>

# --- Docker-compose layer management ---
.PHONY: start-dev-env
start-dev-env:
	@make start-dev-persistent
	@make start-dev-system
	@make start-dev-service

.PHONY: start-dev-service
start-dev-service: docker-compose/service/docker-compose.*.yaml
	@for f in $^; do ARCH=$(ARCH) PWD=$(HOST_PWD) COMPOSE_IGNORE_ORPHANS=True \
	  docker-compose -f $${f} -p "<prefix>-service" up -d --no-recreate || true ; done

.PHONY: start-dev-system
start-dev-system: docker-compose/system/docker-compose.*.yaml
	@for f in $^; do PWD=$(HOST_PWD) COMPOSE_IGNORE_ORPHANS=True \
	  docker-compose -f $${f} -p "<prefix>-system" up -d --no-recreate || true ; done

.PHONY: start-dev-persistent
start-dev-persistent: docker-compose/persistent/docker-compose.*.yaml
	@for f in $^; do COMPOSE_IGNORE_ORPHANS=True \
	  docker-compose -f $${f} -p "<prefix>-system" up -d --no-recreate --no-start || true ; done

.PHONY: stop-dev-env
stop-dev-env:
	COMPOSE_IGNORE_ORPHANS=True docker compose -f docker-compose/service/docker-compose.<abbr>.yaml \
	  -p "<prefix>-service" down

.PHONY: stop-dev-all
stop-dev-all:
	@make stop-dev-service
	@make stop-dev-system

.PHONY: purge-dev-all
purge-dev-all:
	@make stop-dev-all
	@make clean-dev-persistent

.PHONY: stop-dev-service
stop-dev-service: docker-compose/service/docker-compose.*.yaml
	@for f in $^; do COMPOSE_IGNORE_ORPHANS=True docker compose -f $${f} \
	  -p "<prefix>-service" down -v; done

.PHONY: stop-dev-system
stop-dev-system: docker-compose/system/docker-compose.*.yaml
	@for f in $^; do COMPOSE_IGNORE_ORPHANS=True docker compose -f $${f} \
	  -p "<prefix>-system" down -v; done

.PHONY: clean-dev-persistent
clean-dev-persistent: docker-compose/persistent/docker-compose.*.yaml
	@for f in $^; do COMPOSE_IGNORE_ORPHANS=True docker-compose -f $${f} \
	  -p "<prefix>-system" down -v; done
```

**Key implementation details:**
- `HOST_PWD` resolves devcontainer vs host paths for Docker volume mounts
- `COMPOSE_IGNORE_ORPHANS=True` suppresses warnings when services span multiple compose files
- `--no-recreate` prevents overwriting running containers
- `--no-start` for persistent layer creates resources without running containers
- `|| true` allows partial failures (e.g., disabled profiles) without aborting the loop
- Wildcard `docker-compose.*.yaml` auto-discovers all files per layer

### Step 8: Generate Devcontainer Configuration

#### Dockerfile

```dockerfile
ARG <LANG>_VER=<version>
FROM <base-image>:${<LANG>_VER}

# Install development tools
RUN <install-language-tools-and-extensions>

# Install zsh (optional, for better dev experience)
RUN apk add zsh-vcs make && \
    sh -c "$(wget -O- https://github.com/deluan/zsh-in-docker/releases/download/v1.2.1/zsh-in-docker.sh)" -- \
    -t agnoster -p git -p z \
    -p https://github.com/zsh-users/zsh-autosuggestions \
    -p https://github.com/zsh-users/zsh-completions
```

#### devcontainer.json

```jsonc
{
  "name": "<project>",
  "build": {
    "dockerfile": "Dockerfile",
    "args": { /* language/tool versions */ }
  },
  "customizations": {
    "vscode": {
      "extensions": [ /* language extensions, copilot, etc. */ ],
      "settings": {
        "terminal.integrated.defaultProfile.linux": "zsh",
        "launch": {
          "configurations": [
            {
              "name": "Launch <Service>",
              "type": "<lang>",
              "request": "launch",
              "program": "${workspaceFolder}",
              "args": ["--config", "docker-compose/etc/<app>.yaml", "serve"]
            }
          ]
        }
      }
    }
  },
  "features": {
    // Docker-outside-of-Docker: control host Docker from devcontainer
    "ghcr.io/cirolosapio/devcontainers-features/alpine-docker-outside-of-docker:0": {}
  },
  "remoteEnv": {
    // CRITICAL: maps host filesystem path for Docker volume mounts
    "HOST_PROJECT_PATH": "${localWorkspaceFolder}"
  },
  "mounts": [
    // Persistent volume for language package cache (survives rebuild)
    { "source": "<project>-devcontainer", "target": "<pkg-cache-dir>", "type": "volume" }
  ],
  "initializeCommand": "docker volume create <project>-devcontainer"
}
```

**Critical devcontainer patterns:**
- `HOST_PROJECT_PATH` via `remoteEnv` — Makefile reads this to construct Docker volume mounts that reference the **host** filesystem, not the devcontainer filesystem
- `initializeCommand` pre-creates named volumes before container starts
- Docker-outside-of-Docker feature gives Docker CLI access without nested Docker

### Step 9: Generate README

Create `docker-compose/README.md` with:
1. Quick start instructions
2. Service enable/disable guide
3. API testing examples with curl commands
4. Network and port reference table
5. Troubleshooting guide

## Reference: Profile Toggle Mechanism

The `.env` profile mechanism works via docker-compose `profiles`:

```yaml
services:
  my-service:
    profiles:
      - ${MY_SERVICE_DISABLE:-}    # Key mechanism
```

- When `MY_SERVICE_DISABLE=true` → profile becomes `["true"]` → service only starts if `--profile true` is passed (which we never do) → **disabled**
- When `MY_SERVICE_DISABLE` is commented out → profile becomes `[""]` → empty string matches default profile → **enabled**

This allows enabling/disabling services by simply commenting/uncommenting lines in `.env`.

## Checklist

After generating all files, verify:

- [ ] All volume names referenced in `system/` and `service/` are declared in `persistent/`
- [ ] All volumes in `system/` and `service/` are marked `external: true`
- [ ] Network name is consistent across all files
- [ ] IP addresses don't conflict
- [ ] `.env` files have both `*_DISABLE` and `*_RELEASE_DISABLE` for each service
- [ ] Config files in `etc/` reference services by container name (not localhost)
- [ ] `HOST_PROJECT_PATH` is set in devcontainer.json `remoteEnv`
- [ ] Makefile `HOST_PWD` uses `$(or $(HOST_PROJECT_PATH),$(LOCAL_PWD))`
- [ ] `make start-dev-env` runs persistent → system → service in order
- [ ] Devcontainer has Docker-outside-of-Docker feature enabled
