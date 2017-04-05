---
layout: collection
title: TransactionHeader
name: transactionheader
description: A transaction header is part of a transaction and gets created the first time a website visitor adds an item to the basket. A transaction can only contain a single transaction header.
 
---

## TransactionHeader

* [Id](#id)
* [Additional Fields](#additionalfields)
* [AddressIdForTransactionDelivery](#addressidfortransactiondelivery)
* [DispatchGrossRounded](#dispatchgrossrounded)
* [GoodsGrossRounded](#goodsgrossrounded)
* [GoodsNettRounded](#goodsnettrounded)
* [OrderDate](#orderdate)
* [OrderDetailNavigateUrl](#orderdetailnavigateurl)
* [Reference](#reference)
* [StageDescription](#stagedescription)
* [TotalGross](#totalgross)
* [TotalGrossRounded](#totalgrossrounded)
* [TotalNettRounded](#totalnettrounded)
* [TotalNumberOfLines](#totalnumberoflines)
* [TotalQuantity](#totalquantity)
* [TotalWeight](#totalweight)

---

<a name="id"></a>
### Id
Determines the Id of the row.

{% raw %}
```liquid
{{ TransactionHeader.Id }}

```
{% endraw %}

Data Type: int

---

<a name="additionalfields"></a>
### Additional Fields
See the [Additional Fields] model for more details.

{% raw %}
```liquid


```
{% endraw %}

Data Type: [Additional Fields]	Model

__link to the [Additional Fields] Model__

---

<a name="addressidfortransactiondelivery"></a>
### AddressIdForTransactionDelivery
Determines the address id to use for transaction delivery

{% raw %}
```liquid
{{ TransactionHeader.AddressIdForTransactionDelivery }}

```
{% endraw %}

Data Type: int

---

<a name="dispatchgrossrounded"></a>
### DispatchGrossRounded
This field is only populated if the Website has been configured with a TransactionHeader DataDisplay that is set to include currency figures

{% raw %}
```liquid
{{ TransactionHeader.DispatchGrossRounded }}

```
{% endraw %}

Data Type: decimal

---
	
<a name="goodsgrossrounded"></a>
### GoodsGrossRounded
This field is only populated if the Website has been configured with a TransactionHeader DataDisplay that is set to include currency figures.

{% raw %}
```liquid
{{ TransactionHeader.GoodsGrossRounded }}

```
{% endraw %}

Data Type: decimal

---

<a name="goodsnettrounded"></a>
### GoodsNettRounded
This field is only populated if the Website has been configured with a TransactionHeader DataDisplay that is set to include currency figures.

{% raw %}
```liquid
{{ TransactionHeader.GoodsNettRounded }}

```
{% endraw %}

Data Type: decimal

---

<a name="orderdate"></a>
### OrderDate
Determines the date of the transaction created or processed.

{% raw %}
```liquid
{{ TransactionHeader.OrderDate }}

```
{% endraw %}

Data Type: DateTime

---

<a name="orderdetailnavigateurl"></a>
### OrderDetailNavigateUrl
Determines the navigate url for order detail.

{% raw %}
```liquid
{{ TransactionHeader.OrderDetailNavigateUrl }}

```
{% endraw %}

Data Type: string

---

<a name="reference"></a>
### Reference
Determines the unique transaction reference.

{% raw %}
```liquid
{{ TransactionHeader.Reference }}

```
{% endraw %}

Data Type: string

---

<a name="stagedescription"></a>
### StageDescription
Determines the description of the website workkflow stage.

{% raw %}
```liquid
{{ TransactionHeader.StageDescription }}

```
{% endraw %}

Data Type: string

---

<a name="totalgross"></a>
### TotalGross
This field is only populated if the Website has been configured with a TransactionHeader DataDisplay that is set to include currency figures.

{% raw %}
```liquid
{{ TransactionHeader.TotalGross }}

```
{% endraw %}

Data Type: decimal

---

<a name="totalgrossrounded"></a>
### TotalGrossRounded
This field is only populated if the Website has been configured with a TransactionHeader DataDisplay that is set to include currency figures.

{% raw %}
```liquid
{{ TransactionHeader.TotalGrossRounded }}

```
{% endraw %}

Data Type: decimal

---

<a name="totalnettrounded"></a>
### TotalNettRounded
This field is only populated if the Website has been configured with a TransactionHeader DataDisplay that is set to include currency figures.

{% raw %}
```liquid
{{ TransactionHeader.TotalNettRounded }}

```
{% endraw %}

Data Type: decimal

---

<a name="totalnumberoflines"></a>
### TotalNumberOfLines
Determines the total number of lines

{% raw %}
```liquid
{{ TransactionHeader.TotalNumberOfLines }}

```
{% endraw %}

Data Type: int

---

<a name="totalquantity"></a>
### TotalQuantity
Determines the total of the Quantity property of all the TransactionLines that belong to a particular transaction.

{% raw %}
```liquid
{{ TransactionHeader.TotalQuantity }}

```
{% endraw %}

Data Type: decimal

---

<a name="totalweight"></a>
### TotalWeight
Determines the total weight

{% raw %}
```liquid
{{ TransactionHeader.TotalWeight }}

```
{% endraw %}

Data Type: decimal

---