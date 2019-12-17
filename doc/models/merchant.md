## Merchant

Represents a Square seller.

### Structure

`Merchant`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | The Square-issued ID of the merchant. |
| `business_name` | `String` | Optional | The business name of the merchant. |
| `country` | [`String (Country)`](/doc/models/country.md) |  | Indicates the country associated with another entity, such as a business.<br>Values are in [ISO 3166-1-alpha-2 format](http://www.iso.org/iso/home/standards/country_codes.htm). |
| `language_code` | `String` | Optional | The language code associated with the merchant account, in BCP 47 format. |
| `currency` | [`String (Currency)`](/doc/models/currency.md) | Optional | Indicates the associated currency for an amount of money. Values correspond<br>to [ISO 4217](https://wikipedia.org/wiki/ISO_4217). |
| `status` | [`String (Merchant Status)`]($m/MerchantStatus) | Optional | - |

### Example (as JSON)

```json
{
  "id": null,
  "business_name": null,
  "country": "FO",
  "language_code": null,
  "currency": null,
  "status": null
}
```

