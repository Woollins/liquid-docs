---
layout: collection
title: PostalAddressResult
name: postaladdressresult
description: The result of executing an Address Lookup. This will consist of the PostalAddress model as well as the selected address information (including the Address Key). The address key could be a Street Number, Premise Name or Organization Name.
 
---

## PostalAddressResult

* [AddressKey](#addresskey)
* [Organizations](#organizations)
* [PostalAddress](#postaladdress)
* [SelectedAddressLine1](#selectedaddressline1)
* [SelectedAddressLine2](#selectedaddressline2)
* [SelectedAddressLine3](#selectedaddressline3)
* [SelectedAddressLine4](#selectedaddressline4)
* [SelectedAddressLine5](#selectedaddressline5)
* [SelectedOrganizationName](#selectedorganizationname)

---

<a name="addresskey"></a>
### AddressKey
Address key represented by a Street Number, Premise Name or Organization Name.

{% raw %}
```liquid
{{ PostalAddressResult.AddressKey }}

```
{% endraw %}

Data Type: string

---

<a name="organizations"></a>
### Organizations
Address key represented by a Street Number, Premise Name or Organization Name.

{% raw %}
```liquid
{{ PostalAddressResult.Organizations }}

```
{% endraw %}

Data Type: string

---

<a name="postaladdress"></a>
### PostalAddress
Contains address information linked to the chosen Postcode.

{% raw %}
```liquid
{{ PostalAddressResult.PostalAddress }}

```
{% endraw %}

Data Type: PostalAddress Model

__link to PostalAddress Model__

---

<a name="selectedaddressline1"></a>
### SelectedAddressLine1
Determines the Address Line 1 of the selected address.

{% raw %}
```liquid
{{ PostalAddressResult.SelectedAddressLine1 }}

```
{% endraw %}

Data Type: string

---

<a name="selectedaddressline2"></a>
### SelectedAddressLine2
Determines the Address Line 2 of the selected address.

{% raw %}
```liquid
{{ PostalAddressResult.SelectedAddressLine2 }}

```
{% endraw %}

Data Type: string

---

<a name="selectedaddressline3"></a>
### SelectedAddressLine3
Determines the Address Line 3 of the selected address.

{% raw %}
```liquid
{{ PostalAddressResult.SelectedAddressLine3 }}

```
{% endraw %}

Data Type: string

---

<a name="selectedaddressline4"></a>
### SelectedAddressLine4
Determines the Address Line 4 of the selected address.

{% raw %}
```liquid
{{ PostalAddressResult.SelectedAddressLine4 }}

```
{% endraw %}

Data Type: string

---

<a name="selectedaddressline5"></a>
### SelectedAddressLine5
Determines the Address Line 5 of the selected address.

{% raw %}
```liquid
{{ PostalAddressResult.SelectedAddressLine5 }}

```
{% endraw %}

Data Type: string

---

<a name="selectedorganizationname"></a>
### SelectedOrganizationName
Determines the Organization Name of the selected address.

{% raw %}
```liquid
{{ PostalAddressResult.SelectedOrganizationName }}

```
{% endraw %}

Data Type: string

---