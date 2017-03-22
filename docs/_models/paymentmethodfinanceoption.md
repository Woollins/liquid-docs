---
layout: collection
title: PaymentMethodFinanceOption
name: paymentmethodfinanceoption
description: Represents an available finance option that the website user can select when they have elected to pay for their order using a finance method of payment.
 
---

## PaymentMethodFinanceOption

* [AnnualPercentageRate](#annualpercentagerate)
* [CategoryIdForPaymentMethod](#categoryidforpaymentmethod)
* [DepositPercentage](#depositpercentage)
* [Description](#description)
* [FinanceSystemProductCode](#financesystemproductcode)
* [Id](#id)

---

<a name="annualpercentagerate"></a>
### AnnualPercentageRate
Determines the annual percentage rate (APR) of this finance option.

{% raw %}
```liquid
{{ PaymentMethodFinanceOption.AnnualPercentageRate }}

```
{% endraw %}

Data Type: decimal

---

<a name="categoryidforpaymentmethod"></a>
### CategoryIdForPaymentMethod
Determines the category id of the payment method that the finance option is linked to.

{% raw %}
```liquid
{{ PaymentMethodFinanceOption.CategoryIdForPaymentMethod }}

```
{% endraw %}

Data Type: int

---

<a name="depositpercentage"></a>
### DepositPercentage
Determines the percentage deposit required for this finance option.

{% raw %}
```liquid
{{ PaymentMethodFinanceOption.DepositPercentage }}

```
{% endraw %}

Data Type: decimal

---

<a name="description"></a>
### Description
Determines the description of the finance option.

{% raw %}
```liquid
{{ PaymentMethodFinanceOption.Description }}

```
{% endraw %}

Data Type: string

---

<a name="financesystemproductcode"></a>
### FinanceSystemProductCode
Determines the finance system product code associated with this finance option.

{% raw %}
```liquid
{{ PaymentMethodFinanceOption.FinanceSystemProductCode }}

```
{% endraw %}

Data Type: string

---

<a name="id"></a>
### Id
Determines the id of the finance option.

{% raw %}
```liquid
{{ PaymentMethodFinanceOption.Id }}

```
{% endraw %}

Data Type: int

---