---
layout: collection
title: PaymentPortal
name: paymentportal
description: Represents the details required to display a Payment Portal.
 
---

## PaymentPortal

* [IsPay4Later](#ispay4later)
* [NavigateUrl](#navigateurl)
* [NoDispatchServiceLevel](#nodispatchservicelevel)
* [NoShoppingBasket](#noshoppingbasket)
* [PaymentAmount](#paymentamount)

---

<a name="ispay4later"></a>
### IsPay4Later
Determines whether or not the model is for the Pay4Later payment method.

{% raw %}
```liquid
{{ PaymentPortal.IsPay4Later }}

```
{% endraw %}

Data Type: boolean

---

<a name="navigateurl"></a>
### NavigateUrl
Determines the URL to navigate to in order to display the Payment Portal.

{% raw %}
```liquid
{{ PaymentPortal.NavigateUrl }}

```
{% endraw %}

Data Type: string

---

<a name="nodispatchservicelevel"></a>
### NoDispatchServiceLevel
Indicates that no DispatchServiceLevel has been configured against the Shopping Basket.

{% raw %}
```liquid
{{ PaymentPortal.NoDispatchServiceLevel }}

```
{% endraw %}

Data Type: boolean

---

<a name="noshoppingbasket"></a>
### NoShoppingBasket
Indicates that the Shopping Basket is empty, or does not have any lines to be paid for.

{% raw %}
```liquid
{{ PaymentPortal.NoShoppingBasket }}

```
{% endraw %}

Data Type: boolean

---

<a name="paymentamount"></a>
### PaymentAmount
Determines the amount that the Payment Portal is going to capture.

{% raw %}
```liquid
{{ PaymentPortal.PaymentAmount }}

```
{% endraw %}

Data Type: decimal

---