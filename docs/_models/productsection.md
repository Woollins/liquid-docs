---
layout: collection
title: ProductSection
name: productsection
description: Models a Product Section that is available on a Hierarchy Node.
 
---

## ProductSection

* [Id](#id)
* [Name](#name)
* [Code](#code)
* [Description](#description)
* [Details](#details)
* [Heading](#heading)
* [Products](#products)

---

<a name="id"></a>
### Id
Determines the Id of the row.

{% raw %}
```liquid
{{ ProductSection.Id }}

```
{% endraw %}

Data Type: int

---

<a name="name"></a>
### Name
Determines the description fo the Product Section.

{% raw %}
```liquid
{{ ProductSection.Name }}

```
{% endraw %}

Data Type: DataType

---

<a name="code"></a>
### Code
Determines the Code of the Website Product Section.

{% raw %}
```liquid
{{ ProductSection.Code }}

```
{% endraw %}

Data Type: string

---

<a name="description"></a>
### Description
Determines the Description of the Website Product Section.

{% raw %}
```liquid
{{ ProductSection.Description }}

```
{% endraw %}

Data Type: string

---
 
<a name="details"></a>
### Details
Determines the Details field specified against the specific hierarchy node.

{% raw %}
```liquid
{{ ProductSection.Details }}

```
{% endraw %}

Data Type: string

---

<a name="heading"></a>
### Heading
Determines the Heading for the Section that is used on the specific Hierarchy Node.

{% raw %}
```liquid
{{ ProductSection.Heading }}

```
{% endraw %}

Data Type: string

---

<a name="products"></a>
### Products
Determines the Products that are available for this Product Section.

{% raw %}
```liquid
{{ ProductSection.Products }}

```
{% endraw %}

Data Type: Product Model

__link to the Product Model__

---