## Catalog Query Items for Item Options

### Structure

`CatalogQueryItemsForItemOptions`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `item_option_ids` | `Array<String>` | Optional | A set of [CatalogItemOption](./models/catalog-item.mdoption) IDs to be used to find associated<br>[CatalogItem](./models/catalog-item.md)s. All Items that contain all of the given Item Options (in any order)<br>will be returned. |

### Example (as JSON)

```json
{
  "item_option_ids": null
}
```

