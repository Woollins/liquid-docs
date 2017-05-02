---
layout: collection
title: Website
name: website
description: Provides access to general properties associated with the website.
 
---

## Website

* [CategoryIdForDefaultCountry](#categoryidfordefaultcountry)
* [CategoryIdForWebsite](#categoryidforwebsite)
* [CategoryUsageIdForAddressCountry](#categoryusageidforaddresscountry)
* [Code](#code)
* [Countries](#countries)
* [Description](#description)
* [HorizontalPriceMatrices](#horizontalpricematrices)
* [PaymentMethods](#paymentmethods)
* [PostalRules](#postalrules)
* [StaticContentUrl](#staticcontenturl)
* [WorkflowDivisionRule](#workflowdivisionrule)

---

<a name="categoryidfordefaultcountry"></a>
### CategoryIdForDefaultCountry
Determines the category id for default country.

{% raw %}
```liquid
{{ Website.CategoryIdForDefaultCountry }}

```
{% endraw %}

Data Type: int

---

<a name="categoryidforwebsite"></a>
### CategoryIdForWebsite
Determines the id of the category that the website is linked to.

{% raw %}
```liquid
{{ Website.CategoryIdForWebsite }}

```
{% endraw %}

Data Type: int

---

<a name="categoryusageidforaddresscountry"></a>
### CategoryUsageIdForAddressCountry
Determines the CategoryUsageIdForAddressCountry specified in the Company Rule row.

{% raw %}
```liquid
{{ Website.CategoryUsageIdForAddressCountry }}

```
{% endraw %}

Data Type: int

---

<a name="code"></a>
### Code
Determines the website code

{% raw %}
```liquid
{{ Website.Code }}

```
{% endraw %}

Data Type: string

---

<a name="countries"></a>
### Countries
Determines the countries available to the website.

{% raw %}
```liquid
{{ Website.Countries }}

```
{% endraw %}

Data Type: AddressCountry Model

__link to the AddressCountry Model__

---

<a name="description"></a>
### Description
Determines the brief description of the website.

{% raw %}
```liquid
{{ Website.Description }}

```
{% endraw %}

Data Type: string

---

<a name="horizontalpricematrices"></a>
### HorizontalPriceMatrices
Determines the Horizontal price matrices available to the website.

{% raw %}
```liquid
{{ Website.HorizontalPriceMatrices }}

```
{% endraw %}

Data Type: PriceMatrix Model

__link to the PriceMatrix Model__

---

<a name="paymentmethods"></a>
### PaymentMethods
Determines one or more payment methods that are available. The first payment method in the list will always be the debit/credit card payment method.

{% raw %}
```liquid
{{ Website.PaymentMethods }}

```
{% endraw %}

Data Type: PaymentMethod Model

__link to the PaymentMethod Model__

---

<a name="postalrules"></a>
### PostalRules
Determines all Postal Rules

{% raw %}
```liquid
{{ Website.PostalRules }}

```
{% endraw %}

Data Type: PostalRule Model

__link to the PostalRule Model__

---

<a name="staticcontenturl"></a>
### StaticContentUrl
Determines the URL where StaticContent such as images can be loaded from.

{% raw %}
```liquid
{{ Website.StaticContentUrl }}

```
{% endraw %}

Data Type: string

---	
		
<a name="workflowdivisionrule"></a>
### WorkflowDivisionRule
Determines the workflow division rule for the company division linked to the website.

{% raw %}
```liquid
{{ Website.WorkflowDivisionRule }}

```
{% endraw %}

Data Type: WorkflowDivisionRule Model

__link to the WorkflowDivisionRule Model__

---	