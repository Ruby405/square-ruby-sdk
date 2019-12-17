## Register Domain Response

Defines the fields that are included in the response body of
a request to the __RegisterDomain__ endpoint.

Either `errors` or `status` will be present in a given response (never both).

### Structure

`RegisterDomainResponse`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `errors` | [`Array<Error Hash>`](/doc/models/error.md) | Optional | Any errors that occurred during the request. |
| `status` | [`String (Register Domain Response Status)`]($m/RegisterDomainResponseStatus) | Optional | The status of domain registration. |

### Example (as JSON)

```json
{
  "status": "VERIFIED"
}
```

