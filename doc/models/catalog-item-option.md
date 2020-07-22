## Catalog Item Option

A group of variations for a `CatalogItem`.

### Structure

`CatalogItemOption`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Optional | The item option's display name for the seller. Must be unique across<br>all item options. This is a searchable attribute for use in applicable query filters. |
| `display_name` | `String` | Optional | The item option's display name for the customer. This is a searchable attribute for use in applicable query filters. |
| `description` | `String` | Optional | The item option's human-readable description. Displayed in the Square<br>Point of Sale app for the seller and in the Online Store or on receipts for<br>the buyer. This is a searchable attribute for use in applicable query filters. |
| `show_colors` | `Boolean` | Optional | If true, display colors for entries in `values` when present. |
| `values` | [`Array<Catalog Object Hash>`](/doc/models/catalog-object.md) | Optional | A list of CatalogObjects containing the<br>`CatalogItemOptionValue`s for this item. |
| `item_count` | `Long` | Optional | The number of `CatalogItem`s currently associated<br>with this item option. Present only if the `include_counts` was specified<br>in the request. Any count over 100 will be returned as `100`. |

### Example (as JSON)

```json
{
  "name": null,
  "display_name": null,
  "description": null,
  "show_colors": null,
  "values": null,
  "item_count": null
}
```

