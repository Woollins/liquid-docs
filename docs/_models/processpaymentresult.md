---
layout: collection
title: ProcessPaymentResult
name: processpaymentresult
description: The result of attempting to process a payment via an alternative payment method.
 
---

## ProcessPaymentResult

* [PaymentCouldNotBeStarted](#paymentcouldnotbestarted)
* [PaymentFailed](#paymentfailed)
* [RedirectUrl](#redirecturl)
* [RedirectUrlNotFound](#redirecturlnotfound)

---

<a name="paymentcouldnotbestarted"></a>
### PaymentCouldNotBeStarted
Will be true if a payment could not be started.

{% raw %}
```liquid
{{ ProcessPaymentResult.PaymentCouldNotBeStarted }}

```
{% endraw %}

Data Type: boolean

---

<a name="paymentfailed"></a>
### PaymentFailed
Will be true if the payment failed to process.

{% raw %}
```liquid
{{ ProcessPaymentResult.PaymentFailed }}

```
{% endraw %}

Data Type: boolean

---

<a name="redirecturl"></a>
### RedirectUrl
Determines the Url to redirect to for payment completion.

{% raw %}
```liquid
{{ ProcessPaymentResult.RedirectUrl }}

```
{% endraw %}

Data Type: string

---

<a name="redirecturlnotfound"></a>
### RedirectUrlNotFound
Will be true if the payment method redirect url has not been found.

{% raw %}
```liquid
{{ ProcessPaymentResult.RedirectUrlNotFound }}

```
{% endraw %}

Data Type: boolean

---	