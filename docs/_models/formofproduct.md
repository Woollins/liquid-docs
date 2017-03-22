---
layout: collection
title: FormOfProduct
name: formofproduct
description: Used internally by the product model to determine what the type of product is. 
 
---

## FormOfProduct

* [IsCollection](#iscollection)
* [IsStandard](#isstandard)
* [IsVariant](#isvariant)
* [IsVariantBase](#isvariantbase)

---

<a name="iscollection"></a>
### IsCollection
True if the product is a collection product.

{% raw %}
```liquid
{{ FormOfProduct.IsCollection }}

```
{% endraw %}

Data Type: string

---

<a name="isstandard"></a>
### IsStandard
True if the product is a standard product.

{% raw %}
```liquid
{{ FormOfProduct.IsStandard }}

```
{% endraw %}

Data Type: boolean

---

<a name="isvariant"></a>
### IsVariant
True if the product is a variant.

{% raw %}
```liquid
{{ FormOfProduct.IsVariant }}

```
{% endraw %}

Data Type: boolean

---

<a name="isvariantbase"></a>
### IsVariantBase
True if the product is the base product of a one or more variant products.

{% raw %}
```liquid
{{ FormOfProduct.IsVariantBase }}

```
{% endraw %}

Data Type: boolean

---


See the Product mode for details.
__ link to Product model__