## Payment

Represents a payment processed by the Square API.

### Structure

`Payment`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` |  | Unique ID for the payment. |
| `created_at` | `String` | Optional | Timestamp of when the payment was created, in RFC 3339 format. |
| `updated_at` | `String` | Optional | Timestamp of when the payment was last updated, in RFC 3339 format. |
| `amount_money` | [`Money Hash`](/doc/models/money.md) |  | Represents an amount of money.<br><br>__Important:__ Unlike version 1 of the Connect API, __all monetary amounts<br>returned by v2 endpoints are positive.__ (In v1, monetary amounts are negative<br>if they represent money being paid _by_ a merchant, instead of money being<br>paid _to_ a merchant.) |
| `tip_money` | [`Money Hash`](/doc/models/money.md) | Optional | Represents an amount of money.<br><br>__Important:__ Unlike version 1 of the Connect API, __all monetary amounts<br>returned by v2 endpoints are positive.__ (In v1, monetary amounts are negative<br>if they represent money being paid _by_ a merchant, instead of money being<br>paid _to_ a merchant.) |
| `total_money` | [`Money Hash`](/doc/models/money.md) | Optional | Represents an amount of money.<br><br>__Important:__ Unlike version 1 of the Connect API, __all monetary amounts<br>returned by v2 endpoints are positive.__ (In v1, monetary amounts are negative<br>if they represent money being paid _by_ a merchant, instead of money being<br>paid _to_ a merchant.) |
| `app_fee_money` | [`Money Hash`](/doc/models/money.md) | Optional | Represents an amount of money.<br><br>__Important:__ Unlike version 1 of the Connect API, __all monetary amounts<br>returned by v2 endpoints are positive.__ (In v1, monetary amounts are negative<br>if they represent money being paid _by_ a merchant, instead of money being<br>paid _to_ a merchant.) |
| `processing_fee` | [`Array<Processing Fee Hash>`](/doc/models/processing-fee.md) | Optional | Processing fees and fee adjustments assessed by Square on this payment. |
| `refunded_money` | [`Money Hash`](/doc/models/money.md) | Optional | Represents an amount of money.<br><br>__Important:__ Unlike version 1 of the Connect API, __all monetary amounts<br>returned by v2 endpoints are positive.__ (In v1, monetary amounts are negative<br>if they represent money being paid _by_ a merchant, instead of money being<br>paid _to_ a merchant.) |
| `status` | `String` | Optional | Indicates whether the payment is `APPROVED`, `COMPLETED`, `CANCELED`, or `FAILED`. |
| `source_type` | `String` | Optional | The source type for this payment |
| `card_details` | [`Card Payment Details Hash`](/doc/models/card-payment-details.md) | Optional | Reflects the current status of a card payment. |
| `location_id` | `String` | Optional | ID of the location associated with the payment. |
| `order_id` | `String` | Optional | ID of the order associated with this payment. |
| `reference_id` | `String` | Optional | An optional ID that associates this payment with an entity in<br>another system. |
| `customer_id` | `String` | Optional | An optional customer_id to be entered by the developer when creating a payment. |
| `refund_ids` | `Array<String>` | Optional | List of `refund_id`s identifying refunds for this payment. |
| `buyer_email_address` | `String` | Optional | The buyer's e-mail address |
| `billing_address` | [`Address Hash`](/doc/models/address.md) | Optional | Represents a physical address. |
| `shipping_address` | [`Address Hash`](/doc/models/address.md) | Optional | Represents a physical address. |
| `note` | `String` | Optional | An optional note to include when creating a payment |

### Example (as JSON)

```json
{
  "id": "id0",
  "created_at": null,
  "updated_at": null,
  "amount_money": {
    "amount": null,
    "currency": null
  },
  "tip_money": null,
  "total_money": null,
  "app_fee_money": null,
  "processing_fee": null,
  "refunded_money": null,
  "status": null,
  "source_type": null,
  "card_details": null,
  "location_id": null,
  "order_id": null,
  "reference_id": null,
  "customer_id": null,
  "refund_ids": null,
  "buyer_email_address": null,
  "billing_address": null,
  "shipping_address": null,
  "note": null
}
```

