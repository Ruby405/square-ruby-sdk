## Search Orders Fulfillment Filter

Filter based on [Order Fulfillment](#type-orderfulfillment) information.

### Structure

`SearchOrdersFulfillmentFilter`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `fulfillment_types` | [`Array<String (Order Fulfillment Type)>`]($m/OrderFulfillmentType) |  | List of [fulfillment types](#type-orderfulfillmenttype) to filter<br>for. Will return orders if any of its fulfillments match any of the fulfillment types<br>listed in this field.<br>See [OrderFulfillmentType](#type-orderfulfillmenttype) for possible values |
| `fulfillment_states` | [`Array<String (Order Fulfillment State)>`]($m/OrderFulfillmentState) | Optional | List of [fulfillment states](#type-orderfulfillmentstate) to filter<br>for. Will return orders if any of its fulfillments match any of the<br>fulfillment states listed in this field.<br>See [OrderFulfillmentState](#type-orderfulfillmentstate) for possible values |

### Example (as JSON)

```json
{
  "fulfillment_types": [
    "SHIPMENT",
    "PICKUP"
  ],
  "fulfillment_states": null
}
```

