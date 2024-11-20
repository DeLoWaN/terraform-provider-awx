---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "awx_credential_vault Resource - terraform-provider-awx"
subcategory: ""
description: |-
  awx_credential_vault manages vault credentials in AWX.
---

# awx_credential_vault (Resource)

`awx_credential_vault` manages vault credentials in AWX.

## Example Usage

```terraform
resource "awx_organization" "example" {
  name = "example"
}

resource "awx_credential_vault" "example" {
  name            = "vault-credential"
  organization_id = awx_organization.example.id
  description     = "This is a vault credential"
  vault_password  = "password"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `name` (String) The name of the credential.
- `vault_password` (String, Sensitive) Vault Password.

### Optional

- `description` (String) The description of the credential.
- `organization_id` (Number) The organization ID this credential belongs to.
- `vault_id` (String) The vault identity to use.

### Read-Only

- `id` (String) The ID of this resource.