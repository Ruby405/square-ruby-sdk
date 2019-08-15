## Search Orders Sort

Sorting options for a query. Returned Orders will always be sorted on a timestamp.

### Structure

`SearchOrdersSort`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sort_field` | [`String (Search Orders Sort Field)`](/doc/models/search-orders-sort-field.md) |  | Specifies which timestamp to use to sort SearchOrder results. |
| `sort_order` | [`String (Sort Order)`](/doc/models/sort-order.md) | Optional | The order (e.g., chronological or alphabetical) in which results from a request are returned. |

### Example (as JSON)

```json
{
  "sort_field": "CLOSED_AT",
  "sort_order": null
}
```

