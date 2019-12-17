## Catalog Info Response

### Structure

`CatalogInfoResponse`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `errors` | [`Array<Error Hash>`](/doc/models/error.md) | Optional | The set of errors encountered. |
| `limits` | [`Catalog Info Response Limits Hash`]($m/CatalogInfoResponseLimits) | Optional | - |
| `standard_unit_description_group` | [`Standard Unit Description Group Hash`]($m/StandardUnitDescriptionGroup) | Optional | Group of standard measurement units. |

### Example (as JSON)

```json
{
  "limits": {
    "batch_upsert_max_objects_per_batch": 1000,
    "batch_upsert_max_total_objects": 10000,
    "batch_retrieve_max_object_ids": 1000,
    "search_max_page_limit": 1000,
    "batch_delete_max_object_ids": 200,
    "update_item_taxes_max_item_ids": 1000,
    "update_item_taxes_max_taxes_to_enable": 1000,
    "update_item_taxes_max_taxes_to_disable": 1000,
    "update_item_modifier_lists_max_item_ids": 1000,
    "update_item_modifier_lists_max_modifier_lists_to_enable": 1000,
    "update_item_modifier_lists_max_modifier_lists_to_disable": 1000
  }
}
```

