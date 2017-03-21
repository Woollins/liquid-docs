---
layout: collection
title: Address
name: address
description: Contains all of the properties associated with an address.
 
---

## Address

* [Id](#id)
* [AddressCode](#addresscode)
* [AddressCountry](#addresscountry)
* [AddressLine1](#addressline1)
* [AddressLine2](#addressline2)
* [AddressLine3](#addressline3)
* [AddressLine4](#addressline4)
* [AddressLine5](#addressline5)
* [DeliveryAddresses](#deliveryaddresses)
* [IsIndividual](#isindividual)
* [OrganisationName](#organisationname)
* [Postcode](#postcode)
* [ProfileNavigateUrl](#profilenavigateurl)

---

<a name="id"></a>
### Id
Determines the Id of the associated data row.

{% raw %}
```liquid
{{ Address.Id }}

```
{% endraw %}

Data Type: int

---

<a name="addresscode"></a>
### AddressCode
Determines the address code, unique to each address

{% raw %}
```liquid
{{ Address.AddressCode }}

```
{% endraw %}

Data Type: string

---

<a name="addresscountry"></a>
### AddressCountry
Determines the country the address resides in.

{% raw %}
```liquid
{{ Address.AddressCountry }}

```
{% endraw %}

Data Type: AddressCountry Model

__link to the AddressCountry Model__

---

<a name="addressline1"></a>
### AddressLine1
Determines the first line of the address.

{% raw %}
```liquid
{{ Address.AddressLine1 }}

```
{% endraw %}

Data Type: string

---

<a name="addressline2"></a>
### AddressLine2
Determines the second line of the address.

{% raw %}
```liquid
{{ Address.AddressLine2 }}

```
{% endraw %}

Data Type: string

---

<a name="addressline3"></a>
### AddressLine3
Determines the third line of the address.

{% raw %}
```liquid
{{ Address.AddressLine3 }}

```
{% endraw %}

Data Type: string

---

<a name="addressline4"></a>
### AddressLine4
Determines the fourth line of the address.

{% raw %}
```liquid
{{ Address.AddressLine4 }}

```
{% endraw %}

Data Type: string

---

<a name="addressline5"></a>
### AddressLine5
Determines the fifth line of the address.

{% raw %}
```liquid
{{ Address.AddressLine5 }}

```
{% endraw %}

Data Type: string

---

<a name="deliveryaddresses"></a>
### DeliveryAddresses
A list of delivery addresses associated with the primary address.

{% raw %}
```liquid
{{ Address.DeliveryAddresses }}

```
{% endraw %}

Data Type: Address	Model

__link to address model__

---

<a name="isindividual"></a>
### IsIndividual
True if the address is for an individual and false if the address is for an organisation.

{% raw %}
```liquid
{{ Address.IsIndividual }}

```
{% endraw %}

Data Type: Boolean

---

<a name="organisationname"></a>
### OrganisationName
Determines the address organisation name.

{% raw %}
```liquid
{{ Address.OrganisationName }}

```
{% endraw %}

Data Type: String

---

<a name="postcode"></a>
### Postcode
Determines the address post code.

{% raw %}
```liquid
{{ Address.Postcode }}

```
{% endraw %}

Data Type: String

---

<a name="profilenavigateurl"></a>
### ProfileNavigateUrl
If the address can be accessed through a profile page, this specifies the navigate Url.

{% raw %}
```liquid
{{ Address.ProfileNavigateUrl }}

```
{% endraw %}

Data Type: String

---