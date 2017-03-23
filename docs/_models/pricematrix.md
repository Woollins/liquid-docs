---
layout: collection
title: PriceMatrix
name: pricematrix
description: Represents a horizontal or vertical price matrix category. Provides access to the category description, code and Id. Price Matrix models can be used to display the available currencies.
 
---

## PriceMatrix

* [CategoryCode](#categorycode)
* [CategoryDescription](#categorydescription)
* [CategoryId](#categoryid)
* [Selected](#selected)

---

<a name="categorycode"></a>
### CategoryCode
Determines the code of the price matrix category.

{% raw %}
```liquid
{{ PriceMatrix.CategoryCode }}

```
{% endraw %}

Data Type: string

---

<a name="categorydescription"></a>
### CategoryDescription
Determines the description of the price matrix category.

{% raw %}
```liquid
{{ PriceMatrix.CategoryDescription }}

```
{% endraw %}

Data Type: string

---

<a name="categoryid"></a>
### CategoryId
Determines the Id of the price matrix category.

{% raw %}
```liquid
{{ PriceMatrix.CategoryId }}

```
{% endraw %}

Data Type: int

---

<a name="selected"></a>
### Selected
Indicates whether this is the Price Matrix that is currently active.

{% raw %}
```liquid
{{ PriceMatrix.Selected }}

```
{% endraw %}

Data Type: boolean

---