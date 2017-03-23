---
layout: collection
title: ProductRegion
name: productregion
description: Represents a Product Price Variance row.
 
---

## ProductRegion

* [Id](#id)
* [Name](#name)
* [Code](#code)
* [Description](#description)
* [Products](#products)

---

<a name="id"></a>
### Id
Determines the Id of the row.

{% raw %}
```liquid
{{ ProductRegion.Id }}

```
{% endraw %}

Data Type: int

---

<a name="name"></a>
### Name
Determines the description of the product region.

{% raw %}
```liquid
{{ ProductRegion.Name }}

```
{% endraw %}

Data Type: DataType

---

<a name="code"></a>
### Code
Determines the product region code.

{% raw %}
```liquid
{{ ProductRegion.Code }}

```
{% endraw %}

Data Type: string

---

<a name="description"></a>
### Description
Determines the description of the product region.

{% raw %}
```liquid
{{ ProductRegion.Description }}

```
{% endraw %}

Data Type: string

---

<a name="products"></a>
### Products
A collection of one or more products that belong to the product region.

{% raw %}
```liquid
{{ ProductRegion.Products }}

```
{% endraw %}

Data Type: Product Model

__link to the Product Model__

---	