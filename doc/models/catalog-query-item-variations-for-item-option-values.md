## Catalog Query Item Variations for Item Option Values

### Structure

`CatalogQueryItemVariationsForItemOptionValues`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `item_option_value_ids` | `Array<String>` | Optional | A set of [CatalogItemOptionValue](./models/catalog-item-option-value.md) IDs to be used to find associated<br>[CatalogItemVariation](./models/catalog-item-variation.md)s. All ItemVariations that contain all of the given<br>Item Option Values (in any order) will be returned. |

### Example (as JSON)

```json
{
  "item_option_value_ids": null
}
```

