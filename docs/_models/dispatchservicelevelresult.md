---
layout: collection
title: DispatchServiceLevelResult
name: dispatchservicelevelresult
description: Describes a dispatch service level providing access to all it's properties.
 
---

## DispatchServiceLevelResult

* [CarrierServiceLevels](#carrierservicelevels)
* [DispatchServiceLevels](#dispatchservicelevels)
* [SelectedCollectionAddressId](#selectedcollectionaddressid)
* [SelectedDispatchServiceLevel](#selecteddispatchservicelevel)
* [ShoppingBasketDispatchServiceLevelModified](#shoppingbasketdispatchservicelevelmodified)

---

<a name="carrierservicelevels"></a>
### CarrierServiceLevels
Determines the available carrier service levels.

{% raw %}
```liquid
{{ DispatchServiceLevelResult.CarrierServiceLevels }}

```
{% endraw %}

Data Type: CarrierServiceLevelItem	Model

__link to CarrierServiceLevelItem	Model__

---

<a name="dispatchservicelevels"></a>
### DispatchServiceLevels
Determines the available dispatch service levels.

{% raw %}
```liquid
{{ DispatchServiceLevelResult.DispatchServiceLevels }}

```
{% endraw %}

Data Type: DispatchServiceLevelItem Model

__link to DispatchServiceLevelItem Model__

---

<a name="selectedcollectionaddressid"></a>
### SelectedCollectionAddressId
Determines the Id of the currently selected collection address.

{% raw %}
```liquid
{{ DispatchServiceLevelResult.SelectedCollectionAddressId }}

```
{% endraw %}

Data Type: int

---

<a name="selecteddispatchservicelevel"></a>
### SelectedDispatchServiceLevel
Determines the selected dispatch service level.

{% raw %}
```liquid
{{ DispatchServiceLevelResult.SelectedDispatchServiceLevel }}

```
{% endraw %}

Data Type: DispatchServiceLevelItem Model

__link to DispatchServiceLevelItem Model__

---

<a name="shoppingbasketdispatchservicelevelmodified"></a>
### ShoppingBasketDispatchServiceLevelModified
Indicates whether the Shopping Basket was modified due to selecting a dispatch service level.

{% raw %}
```liquid
{{ DispatchServiceLevelResult.ShoppingBasketDispatchServiceLevelModified }}

```
{% endraw %}

Data Type: boolean

---