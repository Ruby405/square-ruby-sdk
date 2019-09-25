## Additional Recipient

Represents an additional recipient (other than the merchant) receiving a portion of this tender.

### Structure

`AdditionalRecipient`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location_id` | `String` |  | The location ID for a recipient (other than the merchant) receiving a portion of this tender. |
| `description` | `String` |  | The description of the additional recipient. |
| `amount_money` | [`Money Hash`](/doc/models/money.md) |  | Represents an amount of money. `Money` fields can be signed or unsigned. |
| `receivable_id` | `String` | Optional | The unique ID for this [AdditionalRecipientReceivable](#type-additionalrecipientreceivable), assigned by the server. |

### Example (as JSON)

```json
{
  "location_id": "location_id4",
  "description": "description0",
  "amount_money": {
    "amount": null,
    "currency": null
  },
  "receivable_id": null
}
```

