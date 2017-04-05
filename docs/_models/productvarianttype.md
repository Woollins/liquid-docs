---
layout: collection
title: ProductVariantType
name: productvarianttype
description: Represents a specific Product Variant Type such as Size or Colour.
 
---

## ProductVariantType

* [CategoryIdForProductVariantType](#categoryidforproductvarianttype)
* [Code](#code)
* [Description](#description)
* [EndpointFieldName](#endpointfieldname)
* [Options](#options)

---

<a name="categoryidforproductvarianttype"></a>
### CategoryIdForProductVariantType
Determines the Id of the Category that represents the ProductVariantType. This field will be needed to filter the ProductVariantOption rows to determine the correct Product Id.

{% raw %}
```liquid
{{ ProductVariantType.CategoryIdForProductVariantType }}

```
{% endraw %}

Data Type: int

---

<a name="code"></a>
### Code
Determines the Code of the Category for the ProductVariantType.

{% raw %}
```liquid
{{ ProductVariantType.Code }}

```
{% endraw %}

Data Type: string

---

<a name="description"></a>
### Description
Determines the Description of the Category for the ProductVariantType.

{% raw %}
```liquid
{{ ProductVariantType.Description }}

```
{% endraw %}

Data Type: string

---

<a name="endpointfieldname"></a>
### EndpointFieldName
Determines the name that should be used for the form element when posting the value to the endpoint.

{% raw %}
```liquid
{{ ProductVariantType.EndpointFieldName }}

```
{% endraw %}

Data Type: string

---

<a name="options"></a>
### Options
Determines the Options that are available for the VariantType. The options are sorted and should be displayed in the order in which they are presented.

{% raw %}
```liquid
{{ ProductVariantType.Options }}

```
{% endraw %}

Data Type: ProductVariantOption Model

__link to ProductVariantOption Model__

---