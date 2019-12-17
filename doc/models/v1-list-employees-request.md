## V1 List Employees Request

### Structure

`V1ListEmployeesRequest`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `order` | [`String (Sort Order)`]($m/SortOrder) | Optional | The order (e.g., chronological or alphabetical) in which results from a request are returned. |
| `begin_updated_at` | `String` | Optional | If filtering results by their updated_at field, the beginning of the requested reporting period, in ISO 8601 format |
| `end_updated_at` | `String` | Optional | If filtering results by there updated_at field, the end of the requested reporting period, in ISO 8601 format. |
| `begin_created_at` | `String` | Optional | If filtering results by their created_at field, the beginning of the requested reporting period, in ISO 8601 format. |
| `end_created_at` | `String` | Optional | If filtering results by their created_at field, the end of the requested reporting period, in ISO 8601 format. |
| `status` | [`String (V1 List Employees Request Status)`]($m/V1ListEmployeesRequestStatus) | Optional | - |
| `external_id` | `String` | Optional | If provided, the endpoint returns only employee entities with the specified external_id. |
| `limit` | `Integer` | Optional | The maximum integer number of employee entities to return in a single response. Default 100, maximum 200. |
| `batch_token` | `String` | Optional | A pagination cursor to retrieve the next set of results for your<br>original query to the endpoint. |

### Example (as JSON)

```json
{
  "order": null,
  "begin_updated_at": null,
  "end_updated_at": null,
  "begin_created_at": null,
  "end_created_at": null,
  "status": null,
  "external_id": null,
  "limit": null,
  "batch_token": null
}
```

