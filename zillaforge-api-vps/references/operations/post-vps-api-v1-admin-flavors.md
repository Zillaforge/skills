# POST /vps/api/v1/admin/flavors/

**Resource:** [system_flavor](../resources/system-flavor.md)
**Create Flavor**
**Operation ID:** `post--vps-api-v1-admin-flavors-`

Create a new flavor with specified parameters.

Request body parameters:
- name: Name for this flavor.(required)
- description: Description of this flavor(optional).
- public: Whether the flavor is public (available to all projects) or scoped to a set of projects. Default is False.
- vcpu: The number of virtual CPUs that will be allocated to the server.
- memory: The amount of RAM, in MiB.
- disk: The size of the root disk that will be created in GiB.
- gpu: The info and count of GPUs on each server using this flavor.(optional)
-- model: The model name of GPU from list gpu models api.(required)
-- count: The count of GPUs.
-- is_vgpu: Whether this flavor uses VGPU technology instead of passthoughing physical cards from host machines.
- project_ids: The IDs of one or more projects who can use this flavor if this flavor is private.(optional)
- az: Availability zone where servers are located when they're launched based upon this flavor.(optional)

## Request Body

body data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [admin.FlvCreateInput](../schemas/admin-FlvCreateInput/admin-FlvCreateInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 201 | Created |
| 400 | Bad Request |
| 500 | Internal Server Error |

**Success Response Schema:**

[pb.FlavorInfo](../schemas/pb-FlavorInfo/pb-FlavorInfo.md)

## Security

- **ApiKeyAuth**
