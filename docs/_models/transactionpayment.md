---
layout: collection
title: TransactionPayment
name: transactionpayment
description: The transaction payment model that holds details about the payment.
 
---

## TransactionPayment

* [Amount](#amount)
* [AuthorisationDate](#authorisationdate)
* [MaskedCardNumber](#maskedcardnumber)
* [PaymentMethodDescription](#paymentmethoddescription)
* [Refund](#refund)

---

<a name="amount"></a>
### Amount
Determines the payment amount.

{% raw %}
```liquid
{{ TransactionPayment.Amount }}

```
{% endraw %}

Data Type: decimal

---

<a name="authorisationdate"></a>
### AuthorisationDate
Determines the authorisation date of a payment.

{% raw %}
```liquid
{{ TransactionPayment.AuthorisationDate }}

```
{% endraw %}

Data Type: DateTime

---

<a name="maskedcardnumber"></a>
### MaskedCardNumber
Determines the Masked card number.

{% raw %}
```liquid
{{ TransactionPayment.MaskedCardNumber }}

```
{% endraw %}

Data Type: string

---

<a name="paymentMethoddescription"></a>
### PaymentMethodDescription
Determines the payment method description.

{% raw %}
```liquid
{{ TransactionPayment.PaymentMethodDescription }}

```
{% endraw %}

Data Type: string

---

<a name="refund"></a>
### Refund
Determines if the payment is a refund.

{% raw %}
```liquid
{{ TransactionPayment.Refund }}

```
{% endraw %}

Data Type: boolean

---
