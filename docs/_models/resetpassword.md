---
layout: collection
title: ResetPassword
name: resetpassword
description: Provides access to properties associated with the act of resetting a password.
 
---

## ResetPassword

* [EmailAddress](#emailaddress)
* [EmailAddressNotRegistered](#emailaddressnotregistered)
* [PasswordMismatch](#passwordmismatch)
* [ResetPasswordFailed](#resetpasswordfailed)
* [TemporaryPassword](#temporarypassword)

---

<a name="emailaddress"></a>
### EmailAddress
Determines the email address to reset the password for.

{% raw %}
```liquid
{{ ResetPassword.EmailAddress }}

```
{% endraw %}

Data Type: string

---

<a name="emailaddressnotregistered"></a>
### EmailAddressNotRegistered
Determines if the email address used is not valid.

{% raw %}
```liquid
{{ ResetPassword.EmailAddressNotRegistered }}

```
{% endraw %}

Data Type: boolean

---

<a name="passwordmismatch"></a>
### PasswordMismatch
Determines the new password and confirmation password do not match. This will set the appropriate error message to be displayed.

{% raw %}
```liquid
{{ ResetPassword.PasswordMismatch }}

```
{% endraw %}

Data Type: string

---

<a name="resetpasswordfailed"></a>
### ResetPasswordFailed
Determines the reset password attempt has failed. This will usually happen if the temporary password has been used previously, this is set to display an error message.

{% raw %}
```liquid
{{ ResetPassword.ResetPasswordFailed }}

```
{% endraw %}

Data Type: boolean

---

<a name="temporarypassword"></a>
### TemporaryPassword
Determines the temporary password generated if the email address is valid.

{% raw %}
```liquid
{{ ResetPassword.TemporaryPassword }}

```
{% endraw %}

Data Type: string

---