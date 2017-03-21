---
layout: collection
title: CreateDeliveryAddressResult
name: createdeliveryaddressresult
description: Provides access to properties as a result of creating/trying to create a new delivery address.
 
---

## CreateDeliveryAddressResult

* [DeliveryAddressCouldNotBeCreated](#deliveryaddresscouldnotbecreated)
* [WasSuccessful](#wassuccessful)

---

<a name="deliveryaddresscouldnotbecreated"></a>
### DeliveryAddressCouldNotBeCreated
Will be true if a delivery address could not be created.

{% raw %}
```liquid
{{ CreateDeliveryAddressResult.DeliveryAddressCouldNotBeCreated }}

```
{% endraw %}

Data Type: boolean

---

<a name="wassuccessful"></a>
### WasSuccessful
Indicates that the creation of a delivery address was successful.

{% raw %}
```liquid
{{ CreateDeliveryAddressResult.WasSuccessful }}

```
{% endraw %}

Data Type: boolean

---