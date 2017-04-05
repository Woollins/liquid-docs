---
layout: collection
title: RegistrationResult
name: registrationresult
description: Provides properties to determine whether a registration request was successful or not.
 
---

## RegistrationResult

* [EmailAddressesDoNotMatch](#emailaddressesdonotmatch)
* [GuestRegistraion](#guestregistraion)
* [IsEmailAddressAlreadyRegistered](#isemailaddressalreadyregistered)
* [IsInvalidCountryCode](#isinvalidcountrycode)
* [PasswordsDoNotMatch](#passwordsdonotmatch)
* [SignInDetails](#signindetails)
* [WasSuccessful](#wassuccessful)

---

<a name="emailaddressesdonotmatch"></a>
### EmailAddressesDoNotMatch
The value will be true if the email address and confirmation email address do not match.

{% raw %}
```liquid
{{ RegistrationResult.EmailAddressesDoNotMatch }}

```
{% endraw %}

Data Type: boolean

---

<a name="guestregistraion"></a>
### GuestRegistraion
Will be true if registration for guest.

{% raw %}
```liquid
{{ RegistrationResult.GuestRegistraion }}

```
{% endraw %}

Data Type: boolean

---

<a name="isemailaddressalreadyregistered"></a>
### IsEmailAddressAlreadyRegistered
The value will be true if the email address has already been used to register on the website.

{% raw %}
```liquid
{{ RegistrationResult.IsEmailAddressAlreadyRegistered }}

```
{% endraw %}

Data Type: boolean

---

<a name="isinvalidcountrycode"></a>
### IsInvalidCountryCode
The value will be true if the country code used to register is invalid.

{% raw %}
```liquid
{{ RegistrationResult.IsInvalidCountryCode }}

```
{% endraw %}

Data Type: boolean

---

<a name="passwordsdonotmatch"></a>
### PasswordsDoNotMatch
The value will be true if the password and confirmation password do not match.

{% raw %}
```liquid
{{ RegistrationResult.PasswordsDoNotMatch }}

```
{% endraw %}

Data Type: boolean

---

<a name="signindetails"></a>
### SignInDetails
If the registration request was successful, the website visitor is automatically signed in and the details made available in this model.

{% raw %}
```liquid
{{ RegistrationResult.SignInDetails }}

```
{% endraw %}

Data Type: SignInDetails Model

__link to the SignInDetails Model__

---

<a name="wassuccessful"></a>
### WasSuccessful
Result will be true if the registration request succeeded.

{% raw %}
```liquid
{{ RegistrationResult.WasSuccessful }}

```
{% endraw %}

Data Type: boolean

---