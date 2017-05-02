---
layout: collection
title: ProductPriceVariance
name: productpricevariance
description: Represents a Product Price Variance row.
 
---

## ProductPriceVariance

* [Description](#description)
* [Price](#price)
* [Quantity](#quantity)
* [VatExclusivePrice](#vatexclusiveprice)
* [VatInclusivePrice](#vatinclusiveprice)

---

<a name="description"></a>
### Description
Determines the description for the Price Variance.

{% raw %}
```liquid
{{ ProductPriceVariance.Description }}

```
{% endraw %}

Data Type: string

---

<a name="price"></a>
### Price
Determines the new price to apply if the price variance is triggered. This will be the Vat Inclusive or Vat Exclusive price depending on how the system is setup.

{% raw %}
```liquid
{{ ProductPriceVariance.Price }}

```
{% endraw %}

Data Type: decimal

---

<a name="quantity"></a>
### Quantity
Determines the quantity at which the variance becomes valid.

{% raw %}
```liquid
{{ ProductPriceVariance.Quantity }}

```
{% endraw %}

Data Type: decimal

---

<a name="vatexclusiveprice"></a>
### VatExclusivePrice
Determines the Vat Exclusive Price for the Price variance.

{% raw %}
```liquid
{{ ProductPriceVariance.VatExclusivePrice }}

```
{% endraw %}

Data Type: decimal

---

<a name="vatinclusiveprice"></a>
### VatInclusivePrice
Determines the Vat Inclusive Price for the Price Variance.

{% raw %}
```liquid
{{ ProductPriceVariance.VatInclusivePrice }}

```
{% endraw %}

Data Type: decimal

---