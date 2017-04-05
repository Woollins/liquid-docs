---
layout: collection
title: ResetPasswordConfirmationResult
name: resetpasswordconfirmationresult
description: The result of confirming a password reset.
 
---

## ResetPasswordConfirmationResult

* [EmailAddress](#emailaddress)
* [IsPasswordInvalid](#ispasswordinvalid)
* [IsTemporaryPasswordAlreadyUsed](#istemporarypasswordalreadyused)
* [PasswordsDoNotMatch](#passwordsdonotmatch)
* [ResetPasswordFailed](#resetpasswordfailed)
* [TemporaryPassword](#temporarypassword)

---

<a name="emailaddress"></a>
### EmailAddress
Determines the email address to reset the password for.

{% raw %}
```liquid
{{ ResetPasswordConfirmationResult.EmailAddress }}

```
{% endraw %}

Data Type: string

---

<a name="ispasswordinvalid"></a>
### IsPasswordInvalid
Will be true if the password used in invalid.

{% raw %}
```liquid
{{ ResetPasswordConfirmationResult.IsPasswordInvalid }}

```
{% endraw %}

Data Type: boolean

---

<a name="istemporarypasswordalreadyused"></a>
### IsTemporaryPasswordAlreadyUsed
Will be true if the temporary password has already been used.

{% raw %}
```liquid
{{ ResetPasswordConfirmationResult.IsTemporaryPasswordAlreadyUsed }}

```
{% endraw %}

Data Type: boolean

---

<a name="passwordsdonotmatch"></a>
### PasswordsDoNotMatch
Will be true if the new password and confirmation do not match.

{% raw %}
```liquid
{{ ResetPasswordConfirmationResult.PasswordsDoNotMatch }}

```
{% endraw %}

Data Type: boolean

---

<a name="resetpasswordfailed"></a>
### ResetPasswordFailed
Will be true if the reset password failed.

{% raw %}
```liquid
{{ ResetPasswordConfirmationResult.ResetPasswordFailed }}

```
{% endraw %}

Data Type: boolean

---

<a name="temporarypassword"></a>
### TemporaryPassword
Allows a password to be reset at any time within a given time period as long as the password reset url is available to the user with all of the required parameters.

{% raw %}
```liquid
{{ ResetPasswordConfirmationResult.TemporaryPassword }}

```
{% endraw %}

Data Type: string

---