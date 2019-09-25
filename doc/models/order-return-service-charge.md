## Order Return Service Charge

Represents the service charge applied to the original order.

### Structure

`OrderReturnServiceCharge`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `uid` | `String` | Optional | Unique ID that identifies the return service charge only within this order. |
| `source_service_charge_uid` | `String` | Optional | `uid` of the Service Charge from the Order containing the original<br>charge of the service charge. `source_service_charge_uid` is `null` for<br>unlinked returns. |
| `name` | `String` | Optional | The name of the service charge. |
| `catalog_object_id` | `String` | Optional | The catalog object ID of the associated [CatalogServiceCharge](#type-catalogservicecharge). |
| `percentage` | `String` | Optional | The percentage of the service charge, as a string representation of<br>a decimal number. For example, a value of `"7.25"` corresponds to a<br>percentage of 7.25%.<br><br>Exactly one of `percentage` or `amount_money` should be set. |
| `amount_money` | [`Money Hash`](/doc/models/money.md) | Optional | Represents an amount of money. `Money` fields can be signed or unsigned. |
| `applied_money` | [`Money Hash`](/doc/models/money.md) | Optional | Represents an amount of money. `Money` fields can be signed or unsigned. |
| `total_money` | [`Money Hash`](/doc/models/money.md) | Optional | Represents an amount of money. `Money` fields can be signed or unsigned. |
| `total_tax_money` | [`Money Hash`](/doc/models/money.md) | Optional | Represents an amount of money. `Money` fields can be signed or unsigned. |
| `calculation_phase` | [`String (Order Service Charge Calculation Phase)`](/doc/models/order-service-charge-calculation-phase.md) | Optional | Represents a phase in the process of calculating order totals.<br>Service charges are applied __after__ the indicated phase.<br><br>[Read more about how order totals are calculated.](https://developer.squareup.com/docs/docs/orders-api/how-it-works#how-totals-are-calculated) |
| `taxable` | `Boolean` | Optional | Indicates whether the surcharge can be taxed. Service charges<br>calculated in the `TOTAL_PHASE` cannot be marked as taxable. |
| `return_taxes` | [`Array<Order Return Tax Hash>`](/doc/models/order-return-tax.md) | Optional | Taxes applied to the `OrderReturnServiceCharge`. By default, return-level taxes apply to<br>`OrderReturnServiceCharge`s calculated in the `SUBTOTAL_PHASE` if `taxable` is set to `true`.  On<br>read or retrieve, this list includes both item-level taxes and any return-level taxes<br>apportioned to this item.<br><br>This field has been deprecated in favour of `applied_taxes`. |
| `applied_taxes` | [`Array<Order Line Item Applied Tax Hash>`](/doc/models/order-line-item-applied-tax.md) | Optional | The list of references to `OrderReturnTax` entities applied to the<br>`OrderReturnServiceCharge`. Each `OrderLineItemAppliedTax` has a `tax_uid`<br>that references the `uid` of a top-level `OrderReturnTax` that is being<br>applied to the `OrderReturnServiceCharge`. On reads, the amount applied is<br>populated. |

### Example (as JSON)

```json
{
  "uid": null,
  "source_service_charge_uid": null,
  "name": null,
  "catalog_object_id": null,
  "percentage": null,
  "amount_money": null,
  "applied_money": null,
  "total_money": null,
  "total_tax_money": null,
  "calculation_phase": null,
  "taxable": null,
  "return_taxes": null,
  "applied_taxes": null
}
```

