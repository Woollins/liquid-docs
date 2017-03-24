---
layout: collection
title: ProductVariant
name: productvariant
description: Represents a combination of a VariantType and a VariantOption and the resulting ProductId. For example, a row might exist that indicates that the VariantType SIZE that has a VariantOption of LARGE will have a VariantProductId of 1234. A Variant product will have an entry in this table for each combination of VariantType and VariantOption that produces a product. If there are multiple VariantTypes, then there will be multiple entries for the same variant ProductId for the different available combinations. 
 
---

## ProductVariant

* [CategoryIdForProductVariantType](#categoryidforproductvarianttype)
* [ProductId](#productid)
* [ProductVariantOptionId](#productvariantoptionid)

---

<a name="categoryidforproductvarianttype"></a>
### CategoryIdForProductVariantType
Indicates which Product Variant Type this ProductVariant row is for. For example SIZE.

{% raw %}
```liquid
{{ ProductVariant.CategoryIdForProductVariantType }}

```
{% endraw %}

Data Type: int

---

<a name="productid"></a>
### ProductId
Determines the Id of the Product that is represented by this combination.

{% raw %}
```liquid
{{ ProductVariant.ProductId }}

```
{% endraw %}

Data Type: int

---

<a name="productvariantoptionid"></a>
### ProductVariantOptionId
Determines the Option that was selected such as LARGE.

{% raw %}
```liquid
{{ ProductVariant.ProductVariantOptionId }}

```
{% endraw %}

Data Type: int

---