## Catalog Item

An item (i.e., product family) in the Catalog object model.

### Structure

`CatalogItem`

### Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Optional | The item's name. Searchable. This field must not be empty. This field has max length of 512 Unicode code points. |
| `description` | `String` | Optional | The item's description. Searchable. This field has max length of 4096 Unicode code points. |
| `abbreviation` | `String` | Optional | The text of the item's display label in the Square Point of Sale app. Only up to the first five characters of the string are used. Searchable.<br>This field has max length of 24 Unicode code points. |
| `label_color` | `String` | Optional | The color of the item's display label in the Square Point of Sale app. This must be a valid hex color code. |
| `available_online` | `Boolean` | Optional | If `true`, the item can be added to shipping orders from the merchant's online store. |
| `available_for_pickup` | `Boolean` | Optional | If `true`, the item can be added to pickup orders from the merchant's online store. |
| `available_electronically` | `Boolean` | Optional | If `true`, the item can be added to electronically fulfilled orders from the merchant's online store. |
| `category_id` | `String` | Optional | The ID of the item's category, if any. |
| `tax_ids` | `Array<String>` | Optional | A set of IDs indicating the [CatalogTax](#type-catalogtax)es that are enabled for<br>this item. When updating an item, any taxes listed here will be added to the item.<br>[CatalogTax](#type-catalogtax)es may also be added to or deleted from an item using `UpdateItemTaxes`. |
| `modifier_list_info` | [`Array<Catalog Item Modifier List Info Hash>`](/doc/models/catalog-item-modifier-list-info.md) | Optional | A set of [CatalogItemModifierListInfo](#type-catalogitemmodifierlistinfo) objects<br>representing the modifier lists that apply to this item, along with the overrides and min<br>and max limits that are specific to this item. [CatalogModifierList](#type-catalogmodifierlist)s<br>may also be added to or deleted from an item using `UpdateItemModifierLists`. |
| `variations` | [`Array<Catalog Object Hash>`](/doc/models/catalog-object.md) | Optional | A list of [CatalogObject](#type-catalogobject)s containing the<br>[CatalogItemVariation](#type-catalogitemvariation)s for this item.<br><br>Maximum: 250 item variations |
| `product_type` | [`String (Catalog Item Product Type)`](/doc/models/catalog-item-product-type.md) | Optional | The type of a [CatalogItem](#type-catalogitem). Connect V2 only allows the creation of `REGULAR` or `APPOINTMENTS_SERVICE` items. |
| `skip_modifier_screen` | `Boolean` | Optional | If `false`, the Square Point of Sale app will present the [CatalogItem](#type-catalogitem)'s<br>details screen immediately, allowing the merchant to choose [CatalogModifier](#type-catalogmodifier)s<br>before adding the item to the cart.  This is the default behavior.<br><br>If `true`, the Square Point of Sale app will immediately add the item to the cart with the pre-selected<br>modifiers, and merchants can edit modifiers by drilling down onto the item's details.<br><br>Third-party clients are encouraged to implement similar behaviors. |
| `item_options` | [`Array<Catalog Item Option for Item Hash>`](/doc/models/catalog-item-option-for-item.md) | Optional | List of item options IDs for this item. Used to manage and group item<br>variations in a specified order.<br><br>Maximum: 6 item options. |

### Example (as JSON)

```json
{
  "object": {
    "type": "ITEM",
    "id": "#Cocoa",
    "present_at_all_locations": true,
    "item_data": {
      "name": "Cocoa",
      "description": "Hot chocolate",
      "abbreviation": "Ch",
      "visibility": "PRIVATE"
    }
  }
}
```

