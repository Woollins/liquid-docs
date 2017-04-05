---
layout: collection
title: Transaction
name: transaction
description: A transaction is simply a container for other models that make up the transaction. A transaction is created when a website visitor adds an item to the basket for example. 
 
---

## Transaction

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
{{ Transaction.DeliveryAddress }}

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
{{ Transaction.PrimaryAddress }}

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
{{ Transaction.TransactionHeader }}

```
{% endraw %}


Data Type: TransactionHeader Model

__link to the TransactionHeader	Model__

---

<a name="transactionheadercategories"></a>
### TransactionHeaderCategories
An array of the Categories that are attached to the Transaction Header.

{% raw %}
```liquid
{{ Transaction.TransactionHeaderCategories }}

```
{% endraw %}


Data Type: TransactionHeader Model

__link to the TransactionHeader	Model__

---

<a name="transactionheadercategories"></a>
### TransactionHeaderCategories
An array of the Categories that are attached to the Transaction Header.

{% raw %}
```liquid
{{ Transaction.TransactionHeaderCategories }}

```
{% endraw %}


Data Type: TransactionHeader Model

__link to the TransactionHeader	Model__

---

<a name="transactionlines"></a>
### TransactionLines
A collection of zero or more lines that have been added to the transaction.

{% raw %}
```liquid
{{ Transaction.TransactionLines }}

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
{{ Transaction.TransactionPayments }}

```
{% endraw %}


Data Type: TransactionPayment Model

__link to the TransactionPayment Model__

---