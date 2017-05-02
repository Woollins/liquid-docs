---
layout: collection
title: AddToBasketResult
name: addtobasketresult
description: The result that is returned by the AddToBasket endpoint. Available as a JSON object, but only for JSON post requests.
 
---

## AddToBasketResult

* [IsProductIdValid](#isproductidvalid)
* [IsPurchaseRestricted](#ispurchaserestricted)
* [IsQuantityValid](#isquantityvalid)
* [ProductId](#productid)
* [PurchaseRestrictionMessage](#purchaserestrictionmessage)
* [Quantity](#quantity)
* [WasSuccessful](#wassuccessful)

---

<a name="isproductidvalid"></a>
### IsProductIdValid
True if a valid product id was provided to the endpoint.

{% raw %}
```liquid
{{ AddToBasketResult.IsProductIdValid }}

```
{% endraw %}

Data Type: boolean

---

<a name="ispurchaserestricted"></a>
### IsPurchaseRestricted
True if there is a purchase restriction for the product that would prevent it from being added to the basket.

{% raw %}
```liquid
{{ AddToBasketResult.IsPurchaseRestricted }}

```
{% endraw %}

Data Type: boolean

---
		
<a name="isquantityvalid"></a>
### IsQuantityValid
True if a valid quantity was provided to the endpoint.

{% raw %}
```liquid
{{ AddToBasketResult.IsQuantityValid }}

```
{% endraw %}

Data Type: boolean

---

<a name="productid"></a>
### ProductId
The product id that was provided to the endpoint.

{% raw %}
```liquid
{{ AddToBasketResult.ProductId }}

```
{% endraw %}

Data Type: int

---

<a name="purchaserestrictionmessage"></a>
### PurchaseRestrictionMessage
Contains a message that indicates the reason why the product cannot be purchased.

{% raw %}
```liquid
{{ AddToBasketResult.PurchaseRestrictionMessage }}

```
{% endraw %}

Data Type: string

---

<a name="quantity"></a>
### Quantity
Determines the quantity that was provided to the endpoint.

{% raw %}
```liquid
{{ AddToBasketResult.Quantity }}

```
{% endraw %}

Data Type: decimal

---

<a name="wassuccessful"></a>
### WasSuccessful
True if the add to basket operation completed successfully.

{% raw %}
```liquid
{{ AddToBasketResult.WasSuccessful }}

```
{% endraw %}

Data Type: boolean

---