---
layout: collection
title: ApplyVoucherResult
name: applyvoucherresult
description: Contains the address information of a new user when registering or creating a new delivery address. When a page is posted back, the content in the inputs is lost. This model is used to retain the values entered so that they can be re-populated on a post back.
 
---

## ApplyVoucherResult

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