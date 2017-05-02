---
layout: collection
title: ProductPrice
name: productprice
description: Represents a Price for a Product
 
---

## ProductPrice

* [HorizontalPriceMatrixCategoryId](#horizontalpricematrixcategoryid)
* [HorizontalPriceMatrixCode](#horizontalpricematrixcode)
* [PriceVariances](#pricevariances)
* [ProductId](#productid)
* [VatExclusivePrice](#vatexclusiveprice)
* [VatInclusivePrice](#vatinclusiveprice)
* [VerticalPriceMatrixCategoryId](#verticalpricematrixcategoryid)
* [VerticalPriceMatrixCode](#verticalpricematrixcode)

---

<a name="horizontalpricematrixcategoryid"></a>
### HorizontalPriceMatrixCategoryId
Determines the Id of the Horizontal Price Matrix Category.

{% raw %}
```liquid
{{ ProductPrice.HorizontalPriceMatrixCategoryId }}

```
{% endraw %}

Data Type: int

---

<a name="horizontalpricematrixcode"></a>
### HorizontalPriceMatrixCode
Determines the Code of the Horizontal Price matrix category.

{% raw %}
```liquid
{{ ProductPrice.HorizontalPriceMatrixCode }}

```
{% endraw %}

Data Type: string

---

<a name="pricevariances"></a>
### PriceVariances
Determines the Price Variances for the Price.

{% raw %}
```liquid
{{ ProductPrice.PriceVariances }}

```
{% endraw %}

Data Type: ProductPriceVariance Model

__link to the ProductPriceVariance Model__

---

<a name="productid"></a>
### ProductId
Determines the Id of the Product that this set of price data is for.

{% raw %}
```liquid
{{ ProductPrice.ProductId }}

```
{% endraw %}

Data Type: int

---

<a name="vatexclusiveprice"></a>
### VatExclusivePrice
Determines the Vat Exclusive Price.

{% raw %}
```liquid
{{ ProductPrice.VatExclusivePrice }}

```
{% endraw %}

Data Type: decimal

---

<a name="vatinclusiveprice"></a>
### VatInclusivePrice
Determines the Vat Inclusive price.

{% raw %}
```liquid
{{ ProductPrice.VatInclusivePrice }}

```
{% endraw %}

Data Type: decimal

---

<a name="verticalpricematrixcategoryid"></a>
### VerticalPriceMatrixCategoryId
Determines the Id of the Vertical Price Matrix Category.

{% raw %}
```liquid
{{ ProductPrice.VerticalPriceMatrixCategoryId }}

```
{% endraw %}

Data Type: int

---

<a name="verticalpricematrixcode"></a>
### VerticalPriceMatrixCode
Determines the Code of the Vertical Price Matrix Category.

{% raw %}
```liquid
{{ ProductPrice.VerticalPriceMatrixCode }}

```
{% endraw %}

Data Type: string

---