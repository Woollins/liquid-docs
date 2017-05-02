---
layout: collection
title: CarrierServiceLevelItem
name: carrierservicelevelitem
description: Describes a carrier service level with a list of available delivery dates, the type of service and a cut off time.
 
---

## CarrierServiceLevelItem

* [CategoryIdForCarrierServiceLevel](#categoryidforcarrierservicelevel)
* [CutOffTime](#cutofftime)
* [DeliveryDates](#deliverydates)
* [TypeOfService](#typeofservice)

---

<a name="deliveryaddress"></a>
### CategoryIdForCarrierServiceLevel
Determines the Category Id of the carrier service level.

{% raw %}
```liquid
{{ CarrierServiceLevelItem.CategoryIdForCarrierServiceLevel }}

```
{% endraw %}

Data Type: int

---

<a name="cutofftime"></a>
### CutOffTime
Determines the cut off time after which certain delivery dates are unavailable.

{% raw %}
```liquid
{{ CarrierServiceLevelItem.CutOffTime }}

```
{% endraw %}

Data Type: decimal

---

<a name="deliverydates"></a>
### DeliveryDates
An array/list of available delivery dates.

{% raw %}
```liquid
{{ CarrierServiceLevelItem.DeliveryDates }}

```
{% endraw %}

Data Type: DateTime

---

<a name="typeofservice"></a>
### TypeOfService
Determines the type of service e.g. collection or delivery.

{% raw %}
```liquid
{{ CarrierServiceLevelItem.TypeOfService }}

```
{% endraw %}

Data Type: byte

---