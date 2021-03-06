# QuoteItemOption object

This object describes a filled [product custom option][product-option-object]. It
contains `value` and `label` properties that correspond to the value and label of the custom option
at the time it was filled.

## Personalization properties

The following properties are available for personalization in the `QuoteItemOption` object

| Property name   | Property type                            | Description                                   |
|-----------------|----------------------------------------- |-----------------------------------------------|
| quoteItem       | _[QuoteItem][quote-item-object]_         | The quote item that was used to fill option. |
| option          | _[ProductOption][product-option-object]_ | The original option object.                   |
| value           | _string_                                 | The value.                                    |
| label           | _string_                                 | The label.                                    |


[product-option-object]: ../../magento-integration/object/product-option
[quote-item-object]: ../../magento-integration/object/quote-item
