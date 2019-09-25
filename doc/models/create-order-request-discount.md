## Create Order Request Discount

__Deprecated__: Please use the [OrderLineItemDiscount](#type-orderlineitemdiscount) type
in the order field of [CreateOrderRequest](#type-createorderrequest) instead.

Represents a discount that can apply to either a single line item or an entire order.

### Structure

`CreateOrderRequestDiscount`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `catalog_object_id` | `String` | Optional | Only used for catalog discounts.<br>The catalog object ID for an existing [CatalogDiscount](#type-catalogdiscount).<br><br>Do not provide a value for this field if you provide values in other fields for an ad hoc discount. |
| `name` | `String` | Optional | Only used for ad hoc discounts. The discount's name. |
| `percentage` | `String` | Optional | Only used for ad hoc discounts. The percentage of the discount, as a string representation of a decimal number.<br><br>A value of `7.25` corresponds to a percentage of 7.25%. This value range between 0.0 up to 100.0 |
| `amount_money` | [`Money Hash`](/doc/models/money.md) | Optional | Represents an amount of money. `Money` fields can be signed or unsigned. |

### Example (as JSON)

```json
{
  "catalog_object_id": null,
  "name": null,
  "percentage": null,
  "amount_money": null
}
```

