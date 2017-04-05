---
layout: collection
title: TransactionLine
name: transactionline
description: Forms part of a transaction and is created when a website visitor adds an item to their basket. A transaction can contain zero or more transaction lines.
 
---

## TransactionLine

* [Id](#id)
* [LineValue](#linevalue)
* [LineValueIncludingVat](#linevalueincludinvVat)
* [LineVatValue](#linevatvalue)
* [NettPrice](#nettprice)
* [Price](#price)
* [Product](#product)
* [Quantity](#quantity)

---

<a name="id"></a>
### Id
Determines the Id of the row.

{% raw %}
```liquid
{{ TransactionLine.Id }}

```
{% endraw %}

Data Type: int

---

<a name="linevalue"></a>
### LineValue
Determines the total value of the transaction line. This field is only populated if the Website has been configured with a TransactionLine DataDisplay that is set to include currency figures.

{% raw %}
```liquid
{{ TransactionLine.LineValue }}

```
{% endraw %}

Data Type: decimal

---

<a name="linevalueincludingvat"></a>
### LineValueIncludingVat
Determines the total value of the transaction line including VAT. This field is only populated if the Website has been configured with a TransactionLine DataDisplay that is set to include currency figures.

{% raw %}
```liquid
{{ TransactionLine.LineValueIncludingVat }}

```
{% endraw %}

Data Type: decimal

---

<a name="linevatvalue"></a>
### LineVatValue
Determines the total value of VAT for the transaction line. This field is only populated if the Website has been configured with a TransactionLine DataDisplay that is set to include currency figures.

{% raw %}
```liquid
{{ TransactionLine.LineVatValue }}

```
{% endraw %}

Data Type: decimal

---

<a name="nettprice"></a>
### NettPrice
Determines the price with excluded VAT. This field is only populated if the Website has been configured with a TransactionLine DataDisplay that is set to include currency figures.

{% raw %}
```liquid
{{ TransactionLine.NettPrice }}

```
{% endraw %}

Data Type: decimal

---

<a name="price"></a>
### Price
Determines the price of the product associated with the transaction line. This field is only populated if the Website has been configured with a TransactionLine DataDisplay that is set to include currency figures.

{% raw %}
```liquid
{{ TransactionLine.Price }}

```
{% endraw %}

Data Type: decimal

---

<a name="product"></a>
### Product
Provides access to the attributes of the product that has been added to the transaction line.

{% raw %}
```liquid
{{ TransactionLine.Product }}

```
{% endraw %}

Data Type: Product Model

__link to the Product Model__

---

<a name="quantity"></a>
### Quantity
Determines the quantity of the product.

{% raw %}
```liquid
{{ TransactionLine.Quantity }}

```
{% endraw %}

Data Type: decimal

---