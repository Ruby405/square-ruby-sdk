## Update Customer Request

Defines the body parameters that can be provided in a request to the
UpdateCustomer endpoint.

### Structure

`UpdateCustomerRequest`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `given_name` | `String` | Optional | The customer's given (i.e., first) name. |
| `family_name` | `String` | Optional | The customer's family (i.e., last) name. |
| `company_name` | `String` | Optional | The name of the customer's company. |
| `nickname` | `String` | Optional | A nickname for the customer. |
| `email_address` | `String` | Optional | The customer's email address. |
| `address` | [`Address Hash`](/doc/models/address.md) | Optional | Represents a physical address. |
| `phone_number` | `String` | Optional | The customer's phone number. |
| `reference_id` | `String` | Optional | An optional second ID you can set to associate the customer with an<br>entity in another system. |
| `note` | `String` | Optional | An optional note to associate with the customer. |
| `birthday` | `String` | Optional | The customer birthday in RFC-3339 format. Year is optional,<br>timezone and times are not allowed. Example: `0000-09-01T00:00:00-00:00`<br>for a birthday on September 1st. `1998-09-01T00:00:00-00:00` for a birthday<br>on September 1st 1998. |

### Example (as JSON)

```json
{
  "phone_number": "",
  "email_address": "New.Amelia.Earhart@example.com",
  "note": "updated customer note"
}
```

