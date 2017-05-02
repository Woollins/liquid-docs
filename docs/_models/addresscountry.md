---
layout: collection
title: AddressCountry
name: addresscountry
description: Describes an address country using a Code and Description. Address Country models are used when a website user registers to a particular website or when an address/delivery address is created/edited.
 
---

## AddressCountry

* [CategoryId](#categoryid)
* [CategoryIdForCurrency](#categoryidforcurrency)
* [CategoryIdForPostalRule](#categoryidforpostalrule)
* [Code](#code)
* [Description](#description)

---

<a name="categoryid"></a>
### CategoryId
Determines the Id for country.

{% raw %}
```liquid
{{ AddressCountry.CategoryId }}

```
{% endraw %}

Data Type: int

---

<a name="categoryidforcurrency"></a>
### CategoryIdForCurrency
Determines the Currency category to apply for the country

{% raw %}
```liquid
{{ AddressCountry.CategoryIdForCurrency }}

```
{% endraw %}

Data Type: int

---

<a name="categoryidforpostalrule"></a>
### CategoryIdForPostalRule
Determines the Id of the Category row used for the Postal Rule against this country

{% raw %}
```liquid
{{ AddressCountry.CategoryIdForPostalRule }}

```
{% endraw %}

Data Type: int

---

<a name="categoryidforpostalrule"></a>
### Code
Determines the two digit code representing the country e.g. GB for Great Britain.

{% raw %}
```liquid
{{ AddressCountry.Code }}

```
{% endraw %}

Data Type: string

---

<a name="description"></a>
### Description
Determines the description of the country e.g. Great Britain.

{% raw %}
```liquid
{{ AddressCountry.Description }}

```
{% endraw %}

Data Type: string

---