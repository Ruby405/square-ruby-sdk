## Create Order Request Line Item

__Deprecated__: Please use the [OrderLineItem](#type-orderlineitem) type in the order
field of [CreateOrderRequest](#type-createorderrequest) instead.

Represents a line item to include in an order. Each line item describes
a different product to purchase, with its own quantity and price details.

Line items can either reference objects from the merchant's catalog, or can
alternatively specify a name and price instead.

### Structure

`CreateOrderRequestLineItem`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Optional | Only used for ad hoc line items. The name of the line item. This value cannot exceed 500 characters.<br><br>Do not provide a value for this field if you provide a value for `catalog_object_id`. |
| `quantity` | `String` |  | The quantity to purchase, as a string representation of a number.<br><br>This string must have a positive integer value. |
| `base_price_money` | [`Money Hash`](/doc/models/money.md) | Optional | Represents an amount of money. `Money` fields can be signed or unsigned. |
| `variation_name` | `String` | Optional | Only used for ad hoc line items. The variation name of the line item. This value cannot exceed 255 characters.<br><br>If this value is not set for an ad hoc line item, the default value of `Regular` is used.<br><br>Do not provide a value for this field if you provide a value for the `catalog_object_id`. |
| `note` | `String` | Optional | The note of the line item. This value cannot exceed 500 characters. |
| `catalog_object_id` | `String` | Optional | Only used for Catalog line items.<br>The catalog object ID for an existing [CatalogItemVariation](#type-catalogitemvariation).<br><br>Do not provide a value for this field if you provide a value for `name` and `base_price_money`. |
| `modifiers` | [`Array<Create Order Request Modifier Hash>`](/doc/models/create-order-request-modifier.md) | Optional | Only used for Catalog line items. The modifiers to include on the line item. |
| `taxes` | [`Array<Create Order Request Tax Hash>`](/doc/models/create-order-request-tax.md) | Optional | The taxes to include on the line item. |
| `discounts` | [`Array<Create Order Request Discount Hash>`](/doc/models/create-order-request-discount.md) | Optional | The discounts to include on the line item. |

### Example (as JSON)

```json
{
  "name": null,
  "quantity": "quantity6",
  "base_price_money": null,
  "variation_name": null,
  "note": null,
  "catalog_object_id": null,
  "modifiers": null,
  "taxes": null,
  "discounts": null
}
```

