---
layout: collection
title: Basket
name: basket
description: Contains the items that have been added to basket. A basket is essentially the same as a transaction. 
 
---

## Basket

* [DeliveryAddress](#deliveryaddress)
* [PrimaryAddress](#primaryaddress)
* [TransactionHeader](#transactionheader)
* [TransactionHeaderCategories](#transactionheadercategories)
* [TransactionLines](#transactionlines)
* [TransactionPayments](#transactionpayments)

---

<a name="deliveryaddress"></a>
### DeliveryAddress
Determines the delivery address of transaction.

{% raw %}
```liquid
{{ Basket.DeliveryAddress }}

```
{% endraw %}

Data Type: Address Model

__link to the Address Model__

---

<a name="primaryaddress"></a>
### PrimaryAddress
Determines the primary address for transaction.

{% raw %}
```liquid
{{ Basket.PrimaryAddress }}

```
{% endraw %}

Data Type: Address Model

__link to the Address Model__

---

<a name="transactionheader"></a>
### TransactionHeader
Determines the header part of the transaction.

{% raw %}
```liquid
{{ Basket.TransactionHeader }}

```
{% endraw %}

Data Type: TransactionHeader Model

__link to the TransactionHeader Model__

---

<a name="transactionheadercategories"></a>
### TransactionHeaderCategories
Determines the header part of the transaction.

{% raw %}
```liquid
{{ Basket.TransactionHeaderCategories }}

```
{% endraw %}

Data Type: TransactionHeader Model

__link to the TransactionHeader Model__

---


<a name="transactionlines"></a>
### TransactionLines
A collection of zero or more lines that have been added to the transaction.

{% raw %}
```liquid
{{ Basket.TransactionLines }}

```
{% endraw %}

Data Type: TransactionLine Model

__link to the TransactionLine Model__

---

<a name="transactionpayments"></a>
### TransactionPayments
An array of transaction paymants made.

{% raw %}
```liquid
{{ Basket.TransactionPayments }}

```
{% endraw %}

Data Type: TransactionPayment Model

__link to the TransactionPayment Model__

---



See the Transaction model for details.

__link to the Transaction model__