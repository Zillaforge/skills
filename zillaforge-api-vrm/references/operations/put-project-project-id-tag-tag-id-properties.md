# PUT /project/:{project-id}/tag/:{tag-id}/properties

**Resource:** [User/Tag](../resources/User-Tag.md)
**更新指定 tag 的屬性**
**Operation ID:** `put--project-:{project-id}-tag-:{tag-id}-properties`

Update hardware properties (hw_machine_type, hw_firmware_type, hw_disk_bus) for a specific tag. Only the tag creator, tenant owner, or tenant admin can perform this operation.
<table class="basic-table">
<thead>
<tr>
<th>hw_machine_type</th>
<th>hw_firmware_type</th>
<th>hw_disk_bus</th>
</tr>
</thead>
<tbody>
<tr>
<td>q35</td>
<td>uefi</td>
<td>one of virtio, sata, scsi.</td>
</tr>
<tr>
<td>q35</td>
<td>bios</td>
<td>one of virtio, sata, scsi.</td>
</tr>
<tr>
<td>i440fx</td>
<td>bios</td>
<td>one of virtio, ide.</td>
</tr>
</tbody>
</table>

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `project-id` | path | string | Yes | Project ID |
| `tag-id` | path | string | Yes | Tag ID |

## Request Body

Tag properties update data

**Required:** Yes

**Content Types:** `application/json`

**Schema:** [user.UpdateTagPropertiesInput](../schemas/user-UpdateTagPropertiesInput/user-UpdateTagPropertiesInput.md)

## Responses

| Status | Description |
|--------|-------------|
| 200 | Successfully updated tag properties |
| 400 | Bad request - malformed input |
| 401 | Unauthorized - insufficient permissions |
| 403 | Forbidden |
| 404 | Tag not found |
| 500 | Internal server error |

**Success Response Schema:**

[user.UpdateTagPropertiesOutput](../schemas/user-UpdateTagPropertiesOutput/user-UpdateTagPropertiesOutput.md)

