---
layout: collection
title: UpdateBasketResult
name: updatebasketresult
description: The result that is returned by the UpdateBasket endpoint. Available as a JSON object, but only for JSON post requests.
 
---

## UpdateBasketResult

* [IsPurchaseRestricted](#ispurchaserestricted)
* [IsQuantityValid](#isquantityvalid)
* [IsTransactionLineIdValid](#istransactionlineidvalid)
* [PurchaseRestrictionMessage](#purchaserestrictionmessage)
* [Quantity](#quantity)
* [TransactionLineId](#transactionlineid)
* [WasRemoved](#wasremoved)
* [WasSuccessful](#wassuccessful)

---

<a name="ispurchaserestricted"></a>
### IsPurchaseRestricted
True if there is a purchase restriction for the product that would prevent the quantity from being updated.

{% raw %}
```liquid
{{ UpdateBasketResult.IsPurchaseRestricted }}

```
{% endraw %}

Data Type: boolean

---

<a name="isquantityvalid"></a>
### IsQuantityValid
True if a valid quantity was provided to the endpoint.

{% raw %}
```liquid
{{ UpdateBasketResult.IsQuantityValid }}

```
{% endraw %}

Data Type: boolean

---

<a name="istransactionlineidvalid"></a>
### IsTransactionLineIdValid
True if a valid transaction line id was provided to the endpoint.

{% raw %}
```liquid
{{ UpdateBasketResult.IsTransactionLineIdValid }}

```
{% endraw %}

Data Type: boolean

---

<a name="purchaserestrictionmessage"></a>
### PurchaseRestrictionMessage
Contains a message that indicates the reason why more of the product cannot be purchased.

{% raw %}
```liquid
{{ UpdateBasketResult.PurchaseRestrictionMessage }}

```
{% endraw %}

Data Type: string

---
	
<a name="quantity"></a>
### Quantity
Determines the quantity that was provided to the endpoint.

{% raw %}
```liquid
{{ UpdateBasketResult.Quantity }}

```
{% endraw %}

Data Type: decimal

---

<a name="transactionlineid"></a>
### TransactionLineId
Determines the transaction line id that was provided to the endpoint.

{% raw %}
```liquid
{{ UpdateBasketResult.TransactionLineId }}

```
{% endraw %}

Data Type: int

---

<a name="wasremoved"></a>
### WasRemoved
True if the item was removed from the basket (because a zero quantity was specifieid).

{% raw %}
```liquid
{{ UpdateBasketResult.WasRemoved }}

```
{% endraw %}

Data Type: boolean

---
	
<a name="wassuccessful"></a>
### WasSuccessful
True if the update basket operation completed successfully.

{% raw %}
```liquid
{{ UpdateBasketResult.WasSuccessful }}

```
{% endraw %}

Data Type: boolean

---