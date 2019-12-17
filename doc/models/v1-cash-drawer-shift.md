## V1 Cash Drawer Shift

Contains details for a single cash drawer shift.

### Structure

`V1CashDrawerShift`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | The shift's unique ID. |
| `event_type` | [`String (V1 Cash Drawer Shift Event Type)`]($m/V1CashDrawerShiftEventType) | Optional | - |
| `opened_at` | `String` | Optional | The time when the shift began, in ISO 8601 format. |
| `ended_at` | `String` | Optional | The time when the shift ended, in ISO 8601 format. |
| `closed_at` | `String` | Optional | The time when the shift was closed, in ISO 8601 format. |
| `employee_ids` | `Array<String>` | Optional | The IDs of all employees that were logged into Square Register at some point during the cash drawer shift. |
| `opening_employee_id` | `String` | Optional | The ID of the employee that started the cash drawer shift. |
| `ending_employee_id` | `String` | Optional | The ID of the employee that ended the cash drawer shift. |
| `closing_employee_id` | `String` | Optional | The ID of the employee that closed the cash drawer shift by auditing the cash drawer's contents. |
| `description` | `String` | Optional | A description of the cash drawer shift. |
| `starting_cash_money` | [`V1 Money Hash`]($m/V1Money) | Optional | - |
| `cash_payment_money` | [`V1 Money Hash`]($m/V1Money) | Optional | - |
| `cash_refunds_money` | [`V1 Money Hash`]($m/V1Money) | Optional | - |
| `cash_paid_in_money` | [`V1 Money Hash`]($m/V1Money) | Optional | - |
| `cash_paid_out_money` | [`V1 Money Hash`]($m/V1Money) | Optional | - |
| `expected_cash_money` | [`V1 Money Hash`]($m/V1Money) | Optional | - |
| `closed_cash_money` | [`V1 Money Hash`]($m/V1Money) | Optional | - |
| `device` | [`Device Hash`](/doc/models/device.md) | Optional | - |
| `events` | [`Array<V1 Cash Drawer Event Hash>`]($m/V1CashDrawerEvent) | Optional | All of the events (payments, refunds, and so on) that involved the cash drawer during the shift. |

### Example (as JSON)

```json
{
  "id": null,
  "event_type": null,
  "opened_at": null,
  "ended_at": null,
  "closed_at": null,
  "employee_ids": null,
  "opening_employee_id": null,
  "ending_employee_id": null,
  "closing_employee_id": null,
  "description": null,
  "starting_cash_money": null,
  "cash_payment_money": null,
  "cash_refunds_money": null,
  "cash_paid_in_money": null,
  "cash_paid_out_money": null,
  "expected_cash_money": null,
  "closed_cash_money": null,
  "device": null,
  "events": null
}
```

