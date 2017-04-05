---
layout: collection
title: ProductVariantBase
name: productvariantbase
description: Represents the Variant Information for a Variant Base Product.
 
---

## ProductVariantBase

* [ProductVariants](#productvariants)
* [VariantTypes](#varianttypes)

---

<a name="productvariants"></a>
### ProductVariants
Determines the Variant Combinations that are available for this variant base.

{% raw %}
```liquid
{{ ProductVariantBase.ProductVariants }}

```
{% endraw %}

Data Type: ProductVariant Model

__link to ProductVariant Model__

---

<a name="varianttypes"></a>
### VariantTypes
Determines the Variant Types that are used for this Variant product. These are provided in the correct order for display.

{% raw %}
```liquid
{{ ProductVariantBase.VariantTypes }}

```
{% endraw %}

Data Type: ProductVariantType Model

__link to ProductVariantType Model__

---