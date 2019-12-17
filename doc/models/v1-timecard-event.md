## V1 Timecard Event

V1TimecardEvent

### Structure

`V1TimecardEvent`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | The event's unique ID. |
| `event_type` | [`String (V1 Timecard Event Event Type)`]($m/V1TimecardEventEventType) | Optional | Actions that resulted in a change to a timecard. All timecard<br>events created with the Connect API have an event type that begins with<br>`API`. |
| `clockin_time` | `String` | Optional | The time the employee clocked in, in ISO 8601 format. |
| `clockout_time` | `String` | Optional | The time the employee clocked out, in ISO 8601 format. |
| `created_at` | `String` | Optional | The time when the event was created, in ISO 8601 format. |

### Example (as JSON)

```json
{
  "id": null,
  "event_type": null,
  "clockin_time": null,
  "clockout_time": null,
  "created_at": null
}
```

