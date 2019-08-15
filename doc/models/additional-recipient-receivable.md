## Additional Recipient Receivable

Represents a monetary distribution of part of a [Transaction](./models/transaction.md)'s amount for Transactions which included additional recipients. The location of this receivable is that same as the one specified in the [AdditionalRecipient](./models/additional-recipient.md).

### Structure

`AdditionalRecipientReceivable`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` |  | The additional recipient receivable's unique ID, issued by Square payments servers. |
| `transaction_id` | `String` |  | The ID of the transaction that the additional recipient receivable was applied to. |
| `transaction_location_id` | `String` |  | The ID of the location that created the receivable. This is the location ID on the associated transaction. |
| `amount_money` | [`Money Hash`](/doc/models/money.md) |  | Represents an amount of money.<br><br>__Important:__ Unlike version 1 of the Connect API, __all monetary amounts<br>returned by v2 endpoints are positive.__ (In v1, monetary amounts are negative<br>if they represent money being paid _by_ a merchant, instead of money being<br>paid _to_ a merchant.) |
| `created_at` | `String` | Optional | The time when the additional recipient receivable was created, in RFC 3339 format. |
| `refunds` | [`Array<Additional Recipient Receivable Refund Hash>`](/doc/models/additional-recipient-receivable-refund.md) | Optional | Any refunds of the receivable that have been applied. |

### Example (as JSON)

```json
{
  "id": "id0",
  "transaction_id": "transaction_id8",
  "transaction_location_id": "transaction_location_id6",
  "amount_money": {
    "amount": null,
    "currency": null
  },
  "created_at": null,
  "refunds": null
}
```

