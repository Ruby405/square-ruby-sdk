## V1 Payment Itemization

Payment include an` itemizations` field that lists the items purchased,
along with associated fees, modifiers, and discounts. Each itemization has an
`itemization_type` field that indicates which of the following the itemization
represents:

<ul>
<li>An item variation from the merchant's item library</li>
<li>A custom monetary amount</li>
<li>
An action performed on a Square gift card, such as activating or
reloading it.
</li>
</ul>

*Note**: itemization information included in a `Payment` object reflects
details collected **at the time of the payment**. Details such as the name or
price of items might have changed since the payment was processed.

### Structure

`V1PaymentItemization`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Optional | The item's name. |
| `quantity` | `Float` | Optional | The quantity of the item purchased. This can be a decimal value. |
| `itemization_type` | [`String (V1 Payment Itemization Itemization Type)`]($m/V1PaymentItemizationItemizationType) | Optional | - |
| `item_detail` | [`V1 Payment Item Detail Hash`]($m/V1PaymentItemDetail) | Optional | V1PaymentItemDetail |
| `notes` | `String` | Optional | Notes entered by the merchant about the item at the time of payment, if any. |
| `item_variation_name` | `String` | Optional | The name of the item variation purchased, if any. |
| `total_money` | [`V1 Money Hash`]($m/V1Money) | Optional | - |
| `single_quantity_money` | [`V1 Money Hash`]($m/V1Money) | Optional | - |
| `gross_sales_money` | [`V1 Money Hash`]($m/V1Money) | Optional | - |
| `discount_money` | [`V1 Money Hash`]($m/V1Money) | Optional | - |
| `net_sales_money` | [`V1 Money Hash`]($m/V1Money) | Optional | - |
| `taxes` | [`Array<V1 Payment Tax Hash>`]($m/V1PaymentTax) | Optional | All taxes applied to this itemization. |
| `discounts` | [`Array<V1 Payment Discount Hash>`]($m/V1PaymentDiscount) | Optional | All discounts applied to this itemization. |
| `modifiers` | [`Array<V1 Payment Modifier Hash>`]($m/V1PaymentModifier) | Optional | All modifier options applied to this itemization. |

### Example (as JSON)

```json
{
  "name": null,
  "quantity": null,
  "itemization_type": null,
  "item_detail": null,
  "notes": null,
  "item_variation_name": null,
  "total_money": null,
  "single_quantity_money": null,
  "gross_sales_money": null,
  "discount_money": null,
  "net_sales_money": null,
  "taxes": null,
  "discounts": null,
  "modifiers": null
}
```

