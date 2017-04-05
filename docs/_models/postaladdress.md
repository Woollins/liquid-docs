---
layout: collection
title: PostalAddress
name: postaladdress
description: Contains common fields such as Postcode, Street, Locality as well as lists of Organizations, Street Numbers and Premises.
 
---

## PostalAddress

* [Locality](#locality)
* [Organizations](#organizations)
* [PostalCounty](#postalcounty)
* [Postcode](#postcode)
* [PostTown](#posttown)
* [Premises](#premises)
* [Street](#street)
* [StreetNumbers](#streetnumbers)
* [TraditionalCountry](#traditionalcountry)

---

<a name="locality"></a>
### Locality
Locality associated with the postal address.

{% raw %}
```liquid
{{ PostalAddress.Locality }}

```
{% endraw %}

Data Type: string

---

<a name="organizations"></a>
### Organizations
A list of Organizations associated with the postal rule. This can be null/empty.

{% raw %}
```liquid
{{ PostalAddress.Organizations }}

```
{% endraw %}

Data Type: Organization Model

__link to Organization Model__

---

<a name="postalcounty"></a>
### PostalCounty
Postal Country associated with the postal address.

{% raw %}
```liquid
{{ PostalAddress.PostalCounty }

```
{% endraw %}

Data Type: string

---

<a name="postcode"></a>
### Postcode
Postcode associated with the postal address.

{% raw %}
```liquid
{{ PostalAddress.Postcode }

```
{% endraw %}

Data Type: string

---

<a name="posttown"></a>
### PostTown
Post Town associated with the postal address.

{% raw %}
```liquid
{{ PostalAddress.PostTown }

```
{% endraw %}

Data Type: string

---

<a name="premises"></a>
### Premises
A list of Premises associated with the postal rule. This can be null/empty.

{% raw %}
```liquid
{{ PostalAddress.Premises }

```
{% endraw %}

Data Type: Premise Model

__link to the Premise Model__

---

<a name="street"></a>
### Street
Street associated with the postal address.

{% raw %}
```liquid
{{ PostalAddress.Street }

```
{% endraw %}

Data Type: string

---

<a name="streetnumbers"></a>
### StreetNumbers
A list of Street Numbers associated with the postal address. This can be null/empty.

{% raw %}
```liquid
{{ PostalAddress.StreetNumbers }

```
{% endraw %}

Data Type: StreetNumber Model

__link to StreetNumber Model__

---

<a name="traditionalcountry"></a>
### TraditionalCountry
Traditional Country associated with the postal address.

{% raw %}
```liquid
{{ PostalAddress.TraditionalCountry }

```
{% endraw %}

Data Type: string

---