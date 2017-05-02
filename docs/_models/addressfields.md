---
layout: collection
title: AddressFields
name: addressfields
description: Contains the address information of a new user when registering or creating a new delivery address. When a page is posted back, the content in the inputs is lost. This model is used to retain the values entered so that they can be re-populated on a post back.
 
---

## AddressCountry

* [AddressLine1](#addressline1)
* [AddressLine2](#addressline2)
* [AddressLine3](#addressline3)
* [AddressLine4](#addressline4)
* [AddressLine5](#addressline5)
* [ConfirmationEmailAddress](#confirmationemailaddress)
* [EmailAddress](#emailaddress)
* [FirstName](#firstname)
* [LastName](#lastname)
* [Postcode](#postcode)
* [Title](#title)

---

<a name="addressline1"></a>
### AddressLine1
Determines the first line of the user's address.

{% raw %}
```liquid
{{ AddressFields.AddressLine1 }}

```
{% endraw %}

Data Type: string

---

<a name="addressline2"></a>
### AddressLine2
Determines the second line of the user's address.

{% raw %}
```liquid
{{ AddressFields.AddressLine2 }}

```
{% endraw %}

Data Type: string

---

<a name="addressline3"></a>
### AddressLine3
Determines the third line of the user's address.

{% raw %}
```liquid
{{ AddressFields.AddressLine3 }}

```
{% endraw %}

Data Type: string

---

<a name="addressline4"></a>
### AddressLine4
Determines the fourth line of the user's address.

{% raw %}
```liquid
{{ AddressFields.AddressLine4 }}

```
{% endraw %}

Data Type: string

---

<a name="addressline5"></a>
### AddressLine5
Determines the fifth line of the user's address.

{% raw %}
```liquid
{{ AddressFields.AddressLine5 }}

```
{% endraw %}

Data Type: string

---

<a name="confirmationemailaddress"></a>
### ConfirmationEmailAddress
Determines the confirmation email address of the user.

{% raw %}
```liquid
{{ AddressFields.ConfirmationEmailAddress }}

```
{% endraw %}

Data Type: string

---

<a name="emailaddress"></a>
### EmailAddress
Determines the email address of the user.

{% raw %}
```liquid
{{ AddressFields.EmailAddress }}

```
{% endraw %}

Data Type: string

---

<a name="firstname"></a>
### FirstName
Determines the first name of the user.

{% raw %}
```liquid
{{ AddressFields.FirstName }}

```
{% endraw %}

Data Type: string

---

<a name="lastname"></a>
### LastName
Determines the last name of the user.

{% raw %}
```liquid
{{ AddressFields.LastName }}

```
{% endraw %}

Data Type: string

---

<a name="postcode"></a>
### Postcode
Determines the postcode of the user's address.

{% raw %}
```liquid
{{ AddressFields.Postcode }}

```
{% endraw %}

Data Type: string

---

<a name="title"></a>
### Title
Determines the user's title.

{% raw %}
```liquid
{{ AddressFields.Title }}

```
{% endraw %}

Data Type: string

---