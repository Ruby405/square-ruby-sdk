# Orders

```ruby
orders_api = client.orders
```

## Class Name

`OrdersApi`

## Methods

* [Create Order](/doc/orders.md#create-order)
* [Batch Retrieve Orders](/doc/orders.md#batch-retrieve-orders)
* [Update Order](/doc/orders.md#update-order)
* [Search Orders](/doc/orders.md#search-orders)
* [Pay Order](/doc/orders.md#pay-order)

## Create Order

Creates an [Order](./models/order.md) which specifies products for
purchase, along with discounts, taxes, and other settings to apply to the purchase.

To pay for a created order, please refer to the [Pay for Orders](/orders-api/pay-for-orders)
guide.

You can modify an order after you create it by using the
[UpdateOrder](/doc/orders.md#updateorder) endpoint.  Orders that have reached a terminal state
cannot be updated.

To learn more about the Orders API, see the
[Orders API Overview](/products/orders/overview).

```ruby
def create_order(location_id:,
                 body:)
```

### Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location_id` | `String` | Template, Required | The ID of the business location to associate the order with. |
| `body` | [`Create Order Request Hash`](/doc/models/create-order-request.md) | Body, Required | An object containing the fields to POST for the request.<br><br>See the corresponding object definition for field details. |

### Response Type

[`Create Order Response Hash`](/doc/models/create-order-response.md)

### Example Usage

```ruby
location_id = 'location_id4'
body = {}

result = orders_api.create_order(location_id: location_id, body: body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Batch Retrieve Orders

Retrieves a set of [Order](./models/order.md)s by their IDs.

If a given Order ID does not exist, the ID is ignored instead of generating an error.

```ruby
def batch_retrieve_orders(location_id:,
                          body:)
```

### Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location_id` | `String` | Template, Required | The ID of the orders' associated location. |
| `body` | [`Batch Retrieve Orders Request Hash`](/doc/models/batch-retrieve-orders-request.md) | Body, Required | An object containing the fields to POST for the request.<br><br>See the corresponding object definition for field details. |

### Response Type

[`Batch Retrieve Orders Response Hash`](/doc/models/batch-retrieve-orders-response.md)

### Example Usage

```ruby
location_id = 'location_id4'
body = {}
body[:order_ids] = ['CAISEM82RcpmcFBM0TfOyiHV3es', 'CAISENgvlJ6jLWAzERDzjyHVybY']

result = orders_api.batch_retrieve_orders(location_id: location_id, body: body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Update Order

Updates an [Order](./models/orders.md) by referencing its `order_id` and `version`.

To pay for an order, please refer to the [Pay for Orders](/orders-api/pay-for-orders) guide.

To learn more about the Orders API, see the
[Orders API Overview](/products/orders/overview).

```ruby
def update_order(body:,
                 location_id:,
                 order_id:)
```

### Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`Update Order Request Hash`](/doc/models/update-order-request.md) | Body, Required | An object containing the fields to POST for the request.<br><br>See the corresponding object definition for field details. |
| `location_id` | `String` | Template, Required | - |
| `order_id` | `String` | Template, Required | - |

### Response Type

[`Update Order Response Hash`](/doc/models/update-order-response.md)

### Example Usage

```ruby
body = {}
location_id = 'location_id4'
order_id = 'order_id6'

result = orders_api.update_order(body: body, location_id: location_id, order_id: order_id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Search Orders

Search all Orders for a merchant and return either [Orders](./models/order.md) or
[OrderEntries](./models/order-entries.md).

Note that details for orders processed with Square Point of Sale while in offline mode may not be
transmitted to Square for up to 72 hours. Offline orders have a `created_at` value that reflects
the time the order was originally processed, not the time it was subsequently transmitted to
Square. Consequently, the SearchOrder endpoint might list an offline Order chronologically
between online Orders that were seen in a previous request.

When fetching additional pages using a `cursor`, the `query` must be equal
to the `query` used to fetch the first page of results.

```ruby
def search_orders(body:)
```

### Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`Search Orders Request Hash`](/doc/models/search-orders-request.md) | Body, Required | An object containing the fields to POST for the request.<br><br>See the corresponding object definition for field details. |

### Response Type

[`Search Orders Response Hash`](/doc/models/search-orders-response.md)

### Example Usage

```ruby
body = {}
body[:location_ids] = ['057P5VYJ4A5X1', '18YC4JDH91E1H']
body[:query] = {}
body[:query][:filter] = {}
body[:query][:filter][:state_filter] = {}
body[:query][:filter][:state_filter][:states] = ['COMPLETED']
body[:query][:filter][:date_time_filter] = {}
body[:query][:filter][:date_time_filter][:closed_at] = {}
body[:query][:filter][:date_time_filter][:closed_at][:start_at] = '2018-03-03T20:00:00+00:00'
body[:query][:filter][:date_time_filter][:closed_at][:end_at] = '2019-03-04T21:54:45+00:00'
body[:query][:sort] = {}
body[:query][:sort][:sort_field] = 'CLOSED_AT'
body[:query][:sort][:sort_order] = 'DESC'
body[:limit] = 3
body[:return_entries] = true

result = orders_api.search_orders(body: body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

## Pay Order

Pay for an [order](./models/order.md) using one or more approved [payments](./models/payments.md),
or settle an order with a total of `0`.

The total of the `payments_ids` listed in the request must be equal to the order
total. Orders with a total amount of `0` can be marked as paid by specifying an empty
array of `payment_ids` in the request.

To be used with PayOrder, a payment must:

- Reference the order by specifying the `order_id` when [creating the payment](/doc/payments.md#createpayment).
Any approved payments that reference the same `order_id` not specified in the
`payment_ids` will be canceled.
- Be approved with [delayed capture](/payments-api/take-payments#delayed-capture).
Using a delayed capture payment with PayOrder will complete the approved payment.

Learn how to [pay for orders with a single payment using the Payments API](/orders-api/pay-for-orders).

```ruby
def pay_order(order_id:,
              body:)
```

### Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `order_id` | `String` | Template, Required | The ID of the order being paid. |
| `body` | [`Pay Order Request Hash`](/doc/models/pay-order-request.md) | Body, Required | An object containing the fields to POST for the request.<br><br>See the corresponding object definition for field details. |

### Response Type

[`Pay Order Response Hash`](/doc/models/pay-order-response.md)

### Example Usage

```ruby
order_id = 'order_id6'
body = {}
body[:idempotency_key] = 'c043a359-7ad9-4136-82a9-c3f1d66dcbff'
body[:payment_ids] = ['EnZdNAlWCmfh6Mt5FMNST1o7taB', '0LRiVlbXVwe8ozu4KbZxd12mvaB']

result = orders_api.pay_order(order_id: order_id, body: body)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```

