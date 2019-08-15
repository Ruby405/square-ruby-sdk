## Retrieve Inventory Changes Request

### Structure

`RetrieveInventoryChangesRequest`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location_ids` | `String` | Optional | The [Location](./models/location.md) IDs to look up as a comma-separated<br>list. An empty list queries all locations. |
| `cursor` | `String` | Optional | A pagination cursor returned by a previous call to this endpoint.<br>Provide this to retrieve the next set of results for the original query.<br><br>See [Pagination](https://developer.squareup.com/docs/basics/api101/pagination) for more information. |

### Example (as JSON)

```json
{
  "location_ids": null,
  "cursor": null
}
```

