---
layout: collection
title: WebsiteFormBehaviour
name: websiteformbehaviour
description: Models the Behaviour of a WebsiteForm item
 
---

## WebsiteFormBehaviour

* [IsCreateTransaction](#iscreatetransaction)
* [IsProcessTransaction](#isprocesstransaction)
* [IsTransactionEnquiry](#istransactionenquiry)

---

<a name="iscreatetransaction"></a>
### IsCreateTransaction
Indicates that the Website Form is configured to Create a transaction

{% raw %}
```liquid
{{ WebsiteFormBehaviour.IsCreateTransaction }}

```
{% endraw %}

Data Type: boolean

---

<a name="isprocesstransaction"></a>
### IsProcessTransaction
Indicates that the Website Form is configured to Process a transaction.

{% raw %}
```liquid
{{ WebsiteFormBehaviour.IsProcessTransaction }}

```
{% endraw %}

Data Type: boolean

---
	
<a name="istransactionenquiry"></a>
### IsTransactionEnquiry
Indicates whether the Website Form is an Enquiry type

{% raw %}
```liquid
{{ WebsiteFormBehaviour.IsTransactionEnquiry }}

```
{% endraw %}

Data Type: boolean

---