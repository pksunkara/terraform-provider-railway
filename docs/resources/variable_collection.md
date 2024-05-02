---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "railway_variable_collection Resource - terraform-provider-railway"
subcategory: ""
description: |-
  Railway variable collection. Group of variables managed as a whole. Any changes in collection are triggering service redeployment
---

# railway_variable_collection (Resource)

Railway variable collection. Group of variables managed as a whole. Any changes in collection are triggering service redeployment

## Example Usage

```terraform
resource "railway_variable_collection" "example" {
  environment_id = railway_project.example.default_environment.id
  service_id     = railway_service.example.id

  variables = {
    SENTRY_KEY    = "KEY"
    SENTRY_SECRET = "SECRET"
  }
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `environment_id` (String) Identifier of the environment the variable collection belongs to.
- `service_id` (String) Identifier of the service the variable collection belongs to.
- `variables` (Map of String) Collection of variables.

### Read-Only

- `id` (String) Identifier of the variable collection.

## Import

Import is supported using the following syntax:

```shell
terraform import railway_variable_collection.sentry 89fa0236-2b1b-4a8c-b12d-ae3634b30d97:staging:SENTRY_KEY:SENTRY_SECRET
```