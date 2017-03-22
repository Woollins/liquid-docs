---
layout: collection
title: DispatchServiceLevelItem
name: dispatchservicelevelitem
description: Describes a dispatch service level providing access to all it's properties.
 
---

## DispatchServiceLevelItem

* [CarrierServiceLevelIsCollection](#carrierserviceleveliscollection)
* [CategoryIdForCarrierServiceLevel](#categoryidforcarrierservicelevel)
* [CategoryIdForDispatchServiceLevel](#categoryidfordispatchservicelevel)
* [CategoryIdForDispatchZone](#categoryidfordispatchzone)
* [Charge](#charge)
* [CollectionAddresses](#collectionaddresses)
* [DispatchServiceLevelCode](#dispatchservicelevelcode)
* [DispatchServiceLevelDescription](#dispatchserviceleveldescription)
* [DispatchServiceLevelId](#dispatchservicelevelid)
* [Weight](#weight)

---

<a name="carrierserviceleveliscollection"></a>
### CarrierServiceLevelIsCollection
Determines the Carrier Service Level for the Dispatch Service Level is a Collection From Store service level.

{% raw %}
```liquid
{{ DispatchServiceLevelItem.CarrierServiceLevelIsCollection }}

```
{% endraw %}

Data Type: boolean

---

<a name="categoryidforcarrierservicelevel"></a>
### CategoryIdForCarrierServiceLevel
Determines the Category Id for the Carrier Service Level linked to this Dispatch Service Level.

{% raw %}
```liquid
{{ DispatchServiceLevelItem.CategoryIdForCarrierServiceLevel }}

```
{% endraw %}

Data Type: int

---

<a name="categoryidfordispatchservicelevel"></a>
### CategoryIdForDispatchServiceLevel
Determines the Category Id for the Dispatch Service Level.

{% raw %}
```liquid
{{ DispatchServiceLevelItem.CategoryIdForDispatchServiceLevel }}

```
{% endraw %}

Data Type: int

---

<a name="categoryidfordispatchzone"></a>
### CategoryIdForDispatchZone
Determines the Category Id for the Dispatch Zone.

{% raw %}
```liquid
{{ DispatchServiceLevelItem.CategoryIdForDispatchZone }}

```
{% endraw %}

Data Type: int

---

<a name="charge"></a>
### Charge
Determines the Charge that will be applied for this Dispatch Service Level.

{% raw %}
```liquid
{{ DispatchServiceLevelItem.Charge }}

```
{% endraw %}

Data Type: decimal

---

<a name="collectionaddresses"></a>
### CollectionAddresses
An array of collection addresses. This will only be populated if the dispatch service level is for collection addresses.

{% raw %}
```liquid
{{ DispatchServiceLevelItem.CollectionAddresses }}

```
{% endraw %}

Data Type: Address Model

__link to Address Model__

---

<a name="dispatchservicelevelcode"></a>
### DispatchServiceLevelCode
Determines the Category Code for the Dispatch Service Level.

{% raw %}
```liquid
{{ DispatchServiceLevelItem.DispatchServiceLevelCode }}

```
{% endraw %}

Data Type: string

---

<a name="dispatchserviceleveldescription"></a>
### DispatchServiceLevelDescription
Determines the Category Description for the Dispatch Service Level.

{% raw %}
```liquid
{{ DispatchServiceLevelItem.DispatchServiceLevelDescription }}

```
{% endraw %}

Data Type: string

---

<a name="dispatchservicelevelid"></a>
### DispatchServiceLevelId
Determines the Id of the Dispatch Service Level row.

{% raw %}
```liquid
{{ DispatchServiceLevelItem.DispatchServiceLevelId }}

```
{% endraw %}

Data Type: int

---

<a name="weight"></a>
### Weight
A weight that was returned that was used for calculating the price.

{% raw %}
```liquid
{{ DispatchServiceLevelItem.Weight }}

```
{% endraw %}

Data Type: decimal

---