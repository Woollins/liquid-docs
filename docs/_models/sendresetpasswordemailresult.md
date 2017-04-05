---
layout: collection
title: SendResetPasswordEmailResult
name: sendresetpasswordemailresult
description: Used on the Reset Password Initiation page. If the email address is invalid, the website visitor will be re-directed to the Reset Password Initiation page. 
 
---

## SendResetPasswordEmailResult

* [EmailAddress](#emailaddress)
* [EmailAddressIsNotRegistered](#emailaddressisnotregistered)

---

<a name="emailaddress"></a>
### EmailAddress
Determines the Email Address that was used when starting an attempt to reset the password.

{% raw %}
```liquid
{{ SendResetPasswordEmailResult.EmailAddress }}

```
{% endraw %}

Data Type: string

---

<a name="emailaddressisnotregistered"></a>
### EmailAddressIsNotRegistered
Indicates whether the email address specified in the request is not registered.

{% raw %}
```liquid
{{ SendResetPasswordEmailResult.EmailAddressIsNotRegistered }}

```
{% endraw %}

Data Type: boolean

---