## Order Line Item Modifier

A [CatalogModifier](#type-catalogmodifier).

### Structure

`OrderLineItemModifier`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `uid` | `String` | Optional | Unique ID that identifies the modifier only within this order. |
| `catalog_object_id` | `String` | Optional | The catalog object id referencing [CatalogModifier](#type-catalogmodifier). |
| `name` | `String` | Optional | The name of the item modifier. |
| `base_price_money` | [`Money Hash`](/doc/models/money.md) | Optional | Represents an amount of money. `Money` fields can be signed or unsigned. |
| `total_price_money` | [`Money Hash`](/doc/models/money.md) | Optional | Represents an amount of money. `Money` fields can be signed or unsigned. |

### Example (as JSON)

```json
{
  "uid": null,
  "catalog_object_id": null,
  "name": null,
  "base_price_money": null,
  "total_price_money": null
}
```

