---
layout: collection
title: ProductVariantOption
name: productvariantoption
description: Provides a model containing details of a particular option that is available for a ProductVariant. A Product Variant Option represents a particular option for a ProductVariantType such as LARGE or BLUE.
 
---

## ProductVariantOption

* [Id](#id)
* [Name](#name)
* [Code](#code)
* [Description](#description)

---

<a name="id"></a>
### Id
Determines the Id of the row.

{% raw %}
```liquid
{{ ProductVariantOption.Id }}

```
{% endraw %}

Data Type: int

---

<a name="name"></a>
### Name
Determines the description of the Product Variant Option.

{% raw %}
```liquid
{{ ProductVariantOption.Name }}

```
{% endraw %}

Data Type: DataType

---

<a name="code"></a>
### Code
Determines the Code of the Variant option.

{% raw %}
```liquid
{{ ProductVariantOption.Code }}

```
{% endraw %}

Data Type: string

---

<a name="description"></a>
### Description
Determines the Description of the Variant Option

{% raw %}
```liquid
{{ ProductVariantOption.Description }}

```
{% endraw %}

Data Type: string

---