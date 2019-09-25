## Charge Request Additional Recipient

Represents an additional recipient (other than the merchant) entitled to a portion of the tender.
Support is currently limited to USD, CAD and GBP currencies

### Structure

`ChargeRequestAdditionalRecipient`

### Fields

| Name | Type | Description |
|  --- | --- | --- |
| `location_id` | `String` | The location ID for a recipient (other than the merchant) receiving a portion of the tender. |
| `description` | `String` | The description of the additional recipient. |
| `amount_money` | [`Money Hash`](/doc/models/money.md) | Represents an amount of money. `Money` fields can be signed or unsigned. |

### Example (as JSON)

```json
{
  "location_id": "location_id4",
  "description": "description0",
  "amount_money": {
    "amount": null,
    "currency": null
  }
}
```

