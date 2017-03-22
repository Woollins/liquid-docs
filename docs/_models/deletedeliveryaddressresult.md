---
layout: collection
title: DeleteDeliveryAddressResult
name: deletedeliveryaddressresult
description: Provides access to properties as a result of deleting/trying to delete a delivery address.
 
---

## DeleteDeliveryAddressResult

* [DeliveryAddressCouldNotBeDeleted](#deliveryaddresscouldnotbedeleted)
* [WasSuccessful](#wassuccessful)

---

<a name="deliveryaddresscouldnotbedeleted"></a>
### DeliveryAddressCouldNotBeDeleted
Will be true if a delivery address could not be deleted.

{% raw %}
```liquid
{{ DeleteDeliveryAddressResult.DeliveryAddressCouldNotBeDeleted }}

```
{% endraw %}

Data Type: boolean

---

<a name="deliveryaddresscouldnotbedeleted"></a>
### WasSuccessful
Indicates that the deletion of a delivery address was successful.

{% raw %}
```liquid
{{ DeleteDeliveryAddressResult.WasSuccessful }}

```
{% endraw %}

Data Type: boolean

---