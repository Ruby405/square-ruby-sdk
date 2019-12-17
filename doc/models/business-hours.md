## Business Hours

Represents the hours of operation for a business location.

### Structure

`BusinessHours`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `periods` | [`Array<Business Hours Period Hash>`]($m/BusinessHoursPeriod) | Optional | The list of time periods during which the business is open. There may be at most 10<br>periods per day. |

### Example (as JSON)

```json
{
  "periods": null
}
```

