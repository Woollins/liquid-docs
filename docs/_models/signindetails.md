---
layout: collection
title: SignInDetails
name: signindetails
description: Contains properties for the currently signed-in website visitor. Can be used to display a 'welcome back' message on the site. 
 
---

## SignInDetails

* [AddressContactId](#addresscontactid)
* [AddressId](#addressid)
* [EmailAddress](#emailaddress)
* [FullName](#fullname)
* [GuestSignIn](#guestsignin)
* [SignedIn](#signedin)

---

<a name="addresscontactid"></a>
### AddressContactId
Determines the address contact id of the currently signed-in website visitor.

{% raw %}
```liquid
{{ SignInDetails.AddressContactId }}

```
{% endraw %}

Data Type: int

---

<a name="addressid"></a>
### AddressId
Determines the address id of the currently signed-in website visitor.

{% raw %}
```liquid
{{ SignInDetails.AddressId }}

```
{% endraw %}

Data Type: int

---

<a name="emailaddress"></a>
### EmailAddress
Determines the email address of the currently signed-in website visitor.

{% raw %}
```liquid
{{ SignInDetails.EmailAddress }}

```
{% endraw %}

Data Type: string

---

<a name="fullname"></a>
### FullName
Determines the full name of the currently signed-in website visitor.

{% raw %}
```liquid
{{ SignInDetails.FullName }}

```
{% endraw %}

Data Type: string

---

<a name="guestsignin"></a>
### GuestSignIn
Determines if a user signed in as a guest.

{% raw %}
```liquid
{{ SignInDetails.GuestSignIn }}

```
{% endraw %}

Data Type: boolean

---

<a name="signedin"></a>
### SignedIn
Determines if the model's AddressId and AddressContactId properties are populated, true will be returned.

{% raw %}
```liquid
{{ SignInDetails.SignedIn }}

```
{% endraw %}

Data Type: boolean

---