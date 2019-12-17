## V1 List Orders Request

### Structure

`V1ListOrdersRequest`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `order` | [`String (Sort Order)`]($m/SortOrder) | Optional | The order (e.g., chronological or alphabetical) in which results from a request are returned. |
| `limit` | `Integer` | Optional | The maximum number of payments to return in a single response. This value cannot exceed 200. |
| `batch_token` | `String` | Optional | A pagination cursor to retrieve the next set of results for your<br>original query to the endpoint. |

### Example (as JSON)

```json
{
  "order": null,
  "limit": null,
  "batch_token": null
}
```

