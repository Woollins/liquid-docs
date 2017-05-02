---
layout: collection
title: Address Contact
name: addresscontact
description: Describes an Address Contact providing access to properties.
 
---

## AddressContact

* [Id](#id)
* [Address](#address)
* [Communications](#communications)
* [FirstName](#firstname)
* [FullName](#fullname)
* [LastName](#lastname)
* [MiddleName](#middlename)
* [Sex](#sex)
* [Suffix](#suffix)
* [Title](#title)

---

<a name="id"></a>
### Id
Determines the Id of the associated data row.

{% raw %}
```liquid
{{ AddressContact.Id }}

```
{% endraw %}

Data Type: int

---

<a name="address"></a>
### Address
Determines the address associated with the address contact.

{% raw %}
```liquid
{{ AddressContact.Address }}

```
{% endraw %}

Data Type: Address Model

__link to the address model / might need more info__

---

<a name="communications"></a>
### Communications
A list of communications associated with the contact.

{% raw %}
```liquid
{{ AddressContact.Communications }}

```
{% endraw %}

Data Type: Communication Model

__link to the address model / might need more info__

---

<a name="firstname"></a>
### FirstName
Determines the contact's first name.

{% raw %}
```liquid
{{ AddressContact.FirstName }}

```
{% endraw %}

Data Type: String

---

<a name="fullname"></a>
### FullName
Determines the full name of the contact.

{% raw %}
```liquid
{{ AddressContact.FullName }}

```
{% endraw %}

Data Type: String

---

<a name="lastname"></a>
### LastName
Determines the last name of the contact.

{% raw %}
```liquid
{{ AddressContact.LastName }}

```
{% endraw %}

Data Type: String

---

<a name="middlename"></a>
### MiddleName
Determines the middle name of the contact.

{% raw %}
```liquid
{{ AddressContact.MiddleName }}

```
{% endraw %}

Data Type: String

---

<a name="sex"></a>
### Sex
Determines the sex of the contact.

{% raw %}
```liquid
{{ AddressContact.Sex }}

```
{% endraw %}

Data Type: String

---

<a name="suffix"></a>
### Suffix
Determines the suffix of the contact.

{% raw %}
```liquid
{{ Address.Suffix }}

```
{% endraw %}

Data Type: String

---

<a name="title"></a>
### Title
Determines the title of the contact.

{% raw %}
```liquid
{{ AddressContact.Title }}

```
{% endraw %}

Data Type: String

---