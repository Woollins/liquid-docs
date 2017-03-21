---
layout: collection
title: Payment Method
name: paymentmethod
description: The Payment Method Model holds the details of a Payment Method.
 
---

## Payment Method

* [CategoryIdForPaymentMethod](#categoryidforpaymentmethod)
* [Description](#description)
* [IsCardPayment](#iscardpayment)
* [IsCommideaPayPage](#iscommideapaypage)
* [IsFinancePayment](#isfinancepayment)
* [IsPay4LaterFinance](#ispay4laterfinance)
* [IsPayPalExpress](#ispaypalexpress)
* [IsSagePayServer](#issagepayserver)
* [IsVerifoneWebService](#isverifonewebservice)
* [PaymentMethodFinanceOptions](#paymentmethodfinanceoptions)
* [RequiresRelatedData](#requiresrelateddata)

---

<a name="categoryidforpaymentmethod"></a>
### CategoryIdForPaymentMethod
Determines the Id of the Category that the Payment Method is linked to.

{% raw %}
```liquid
{{ PaymentMethods.CategoryIdForPaymentMethod }}

```
{% endraw %}

Data Type: int

---

<a name="description"></a>
### Description
Determines the description of the Payment Method.

{% raw %}
```liquid
{{ PaymentMethods.Description }}

```
{% endraw %}

Data Type: string

---

<a name="iscardpayment"></a>
### IsCardPayment
Determines whether the method of payment is a credit or debit card.

{% raw %}
```liquid
{{ PaymentMethods.IsCardPayment }}

```
{% endraw %}

Data Type: boolean

---

<a name="iscommideapaypage"></a>
### IsCommideaPayPage
Determines whether the method of payment is configured to use Commidea Pay Page.

{% raw %}
```liquid
{{ PaymentMethods.IsCommideaPayPage }}

```
{% endraw %}

Data Type: boolean

---

<a name="isfinancepayment"></a>
### IsFinancePayment
Determines whether the method of payment is via finance.

{% raw %}
```liquid
{{ PaymentMethods.IsFinancePayment }}

```
{% endraw %}

Data Type: boolean

---

<a name="ispay4laterfinance"></a>
### IsPay4LaterFinance
Determines whether the method of payment is configured to use Pay4Later Finance.

{% raw %}
```liquid
{{ PaymentMethods.IsPay4LaterFinance }}

```
{% endraw %}

Data Type: boolean

---

<a name="ispaypalexpress"></a>
### IsPayPalExpress
Determines whether the method of payment is configured to use Pay Pal Express.

{% raw %}
```liquid
{{ PaymentMethods.IsPayPalExpress }}

```
{% endraw %}

Data Type: boolean

---

<a name="issagepayserver"></a>
### IsSagePayServer
Determines whether the method of payment is configured to use Sage Pay Server.

{% raw %}
```liquid
{{ PaymentMethods.IsSagePayServer }}

```
{% endraw %}

Data Type: boolean

---

<a name="isverifonewebservice"></a>
### IsVerifoneWebService
Determines whether the method of payment is configured to use the Verifone web service.

{% raw %}
```liquid
{{ PaymentMethods.IsVerifoneWebService }}

```
{% endraw %}

Data Type: boolean

---

<a name="paymentmethodfinanceoptions"></a>
### PaymentMethodFinanceOptions
Determines the finance options for this payment method.

{% raw %}
```liquid
{{ PaymentMethods.PaymentMethodFinanceOptions }}

```
{% endraw %}

Data Type: Payment Method Finance Option Model array

__link to Payment Method Finance Option Model array / may need more info__

---

<a name="requiresrelateddata"></a>
### RequiresRelatedData
Indicates if the Payment Method requires Related Data answers to be provided in order to use this payment method. See Get Basket Payment Method Related Data Endpoint for details on how to use this.

{% raw %}
```liquid
{{ PaymentMethods.RequiresRelatedData }}

```
{% endraw %}

Data Type: boolean

__may need more info__

---
	