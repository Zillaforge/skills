---
name: zillaforge-api-guide
description: Reference API documentation for ZillaForge project testing. Use when writing tests, calling APIs, checking request/response schemas, looking up endpoints, authentication flows, or verifying API contracts between services. Covers IAM, VPS, VRM, and other upcoming ZillaForge services. Load this skill when you need to know what endpoints exist, what parameters to pass, or what responses to expect.
---

# ZillaForge API Documentation Reference

## When to Use

Load this skill when you need to:
- Look up an API endpoint path, method, or parameters for supported ZillaForge services (e.g., IAM, VPS, VRM, and more in the future)
- Check request body schema or response structure for a test
- Verify authentication headers or token flows
- Understand available resources (users, projects, memberships, instances, networks, etc.)
- Write integration tests or curl commands against either service

## Available API Skills

*(Note: This list will continue to expand as more services are integrated into ZillaForge.)*

| Service | skills | Description |
|---------|------|-------------|
| IAM (Pegasus IAM) | `zillaforge-api-iam` | Authentication, users, projects, memberships, credentials, MFA, CLI secret, PAAT, SAML |
| VPS (Virtual Platform Service) | `zillaforge-api-vps` | Virtual machines, networks, flavors, floating IPs, storage, admin operations |
| VRM (Virtual Registry Management) | `zillaforge-api-vrm` | Repositories, tags, images, snapshots, project ACLs, member ACLs, export/import/upload |
| *...* | *...* | *(More services to be added)* |

## ⚠️ Host Resolution Rules — ALWAYS Follow This

The `host_ip` and `host_port` values in the skills are **documentation defaults only**. Do **not** use the IP:port from those files directly. **Before using any API, always query the current running environment (e.g., using `docker ps`) to get the actual IP:Port or container_name:Port.**

The correct base URL depends on **where the test is running** (the table below shows typical examples, but always verify first):

| Context | IAM IP:Port | VPS IP:Port | VRM IP:Port | Other Services |
|---------|-------------|-------------|-------------|----------------|
| **Inside devcontainer** (docker-compose network) | `http://iam-server:8084` | `http://vps-server:8106` | `http://vrm-server:8109` | `http://<svc>-server:<port>` |
| **On host machine** (outside devcontainer) | `http://localhost:8084` | `http://localhost:8106` | `http://localhost:8109` | `http://localhost:<port>` |

Container names come from docker-compose:
- IAM: `iam-server` (dev) / `iam-server-release` (release mode), port `8084`
- VPS: `vps-server` (dev) / `vps-server-release` (release mode), port `8106`
- VRM: `vrm-server` (dev) / `vrm-server-release` (release mode), port `8109`
- *(Other services generally follow the `<service_name>-server` convention)*

**Rule**: When generating test code or curl commands, always use a variable or placeholder for the host (e.g., `IAM_HOST`, `VPS_HOST`, `VRM_HOST`, `<SERVICE>_HOST`) rather than hardcoding any IP or `localhost`.




## How to Use During Testing

1. **Determine the actual host and port**: Run `docker ps` in your terminal to check the currently running containers. Use the exact container name (e.g., `iam-server` or `iam-server-release`) and port inside the devcontainer, or `localhost:port` on the host machine. Always assign to a variable, never hardcode.
2. **Get a token first**: Most endpoints require a Bearer token — use `POST /iam/api/v1/login` with `account` + `password`, or use a PAAT.
