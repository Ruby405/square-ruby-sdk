## Order Line Item Applied Tax

Represents an applied portion of a tax to a line item in an order.

Order-scoped taxes automatically include the applied taxes in each line item.
Line item taxes must be referenced from any applicable line items.
The corresponding applied money is automatically computed, based on the
set of participating line items.

### Structure

`OrderLineItemAppliedTax`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `uid` | `String` | Optional | Unique ID that identifies the applied tax only within this order. |
| `tax_uid` | `String` |  | The `uid` of the tax for which this applied tax represents.  Must reference<br>a tax present in the `order.taxes` field.<br><br>This field is immutable. To change which taxes apply to a line item, delete and add new<br>`OrderLineItemAppliedTax`s. |
| `applied_money` | [`Money Hash`](/doc/models/money.md) | Optional | Represents an amount of money. `Money` fields can be signed or unsigned. |

### Example (as JSON)

```json
{
  "uid": null,
  "tax_uid": "tax_uid4",
  "applied_money": null
}
```

