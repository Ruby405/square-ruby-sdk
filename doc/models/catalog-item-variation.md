## Catalog Item Variation

An item variation (i.e., product) in the Catalog object model. Each item
may have a maximum of 250 item variations.

### Structure

`CatalogItemVariation`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `item_id` | `String` | Optional | The ID of the [CatalogItem](./models/catalog-item.md) associated with this item variation. Searchable. |
| `name` | `String` | Optional | The item variation's name. Searchable. This field has max length of 255 Unicode code points. |
| `sku` | `String` | Optional | The item variation's SKU, if any. Searchable. |
| `upc` | `String` | Optional | The item variation's UPC, if any. Searchable in the Connect API.<br>This field is only exposed in the Connect API. It is not exposed in Square's Dashboard,<br>Square Point of Sale app or Retail Point of Sale app. |
| `ordinal` | `Integer` | Optional | The order in which this item variation should be displayed. This value is read-only. On writes, the ordinal<br>for each item variation within a parent [CatalogItem](./models/catalog-item.md) is set according to the item variations's<br>position. On reads, the value is not guaranteed to be sequential or unique. |
| `pricing_type` | [`String (Catalog Pricing Type)`](/doc/models/catalog-pricing-type.md) | Optional | Indicates whether the price of a [CatalogItemVariation](./models/catalog-item-variation.md) should be entered manually at the time of sale. |
| `price_money` | [`Money Hash`](/doc/models/money.md) | Optional | Represents an amount of money.<br><br>__Important:__ Unlike version 1 of the Connect API, __all monetary amounts<br>returned by v2 endpoints are positive.__ (In v1, monetary amounts are negative<br>if they represent money being paid _by_ a merchant, instead of money being<br>paid _to_ a merchant.) |
| `location_overrides` | [`Array<Item Variation Location Overrides Hash>`](/doc/models/item-variation-location-overrides.md) | Optional | Per-[location](./models/location.md) price and inventory overrides. |
| `track_inventory` | `Boolean` | Optional | If `true`, inventory tracking is active for the variation. |
| `inventory_alert_type` | [`String (Inventory Alert Type)`](/doc/models/inventory-alert-type.md) | Optional | Indicates whether Square should alert the merchant when the inventory quantity of a [CatalogItemVariation](./models/catalog-item-variation.md) is low. |
| `inventory_alert_threshold` | `Long` | Optional | If the inventory quantity for the variation is less than or equal to this value and `inventory_alert_type`<br>is `LOW_QUANTITY`, the variation displays an alert in the merchant dashboard.<br><br>This value is always an integer. |
| `user_data` | `String` | Optional | Arbitrary user metadata to associate with the item variation. Cannot exceed 255 characters. Searchable. |
| `service_duration` | `Long` | Optional | If the [CatalogItem](./models/catalog-item.md) that owns this item variation is of type<br>`APPOINTMENTS_SERVICE`, then this is the duration of the service in milliseconds. For<br>example, a 30 minute appointment would have the value `1800000`, which is equal to<br>30 (minutes) * 60 (seconds per minute) * 1000 (milliseconds per second). |
| `item_option_values` | [`Array<Catalog Item Option Value for Item Variation Hash>`](/doc/models/catalog-item-option-value-for-item-variation.md) | Optional | List of item option values associated with this item variation. Listed<br>in the same order as the item options of the parent item. |
| `measurement_unit_id` | `String` | Optional | ID of the ‘CatalogMeasurementUnit’ that is used to measure the quantity<br>sold of this item variation. If left unset, the item will be sold in<br>whole quantities. |

### Example (as JSON)

```json
{
  "item_id": null,
  "name": null,
  "sku": null,
  "upc": null,
  "ordinal": null,
  "pricing_type": null,
  "price_money": null,
  "location_overrides": null,
  "track_inventory": null,
  "inventory_alert_type": null,
  "inventory_alert_threshold": null,
  "user_data": null,
  "service_duration": null,
  "item_option_values": null,
  "measurement_unit_id": null
}
```

