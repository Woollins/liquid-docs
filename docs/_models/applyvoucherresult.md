---
layout: collection
title: ApplyVoucherResult
name: applyvoucherresult
description: The result of applying and removing a voucher. 
 
---

## ApplyVoucherResult

* [AmountLeftToPay](#amountlefttopay)
* [PaymentCoveredByVouchers](#paymentcoveredbyvouchers)
* [VoucherCodeAlreadyRedeemed](#vouchercodealreadyredeemed)
* [VoucherCodeAlreadyRegistered](#vouchercodealreadyregistered)
* [VoucherCodeExpired](#vouchercodeexpired)
* [VoucherCodeInvalid](#vouchercodeinvalid)
* [VoucherCodeNotFound](#vouchercodenotfound)
* [Vouchers](#vouchers)

---

<a name="amountlefttopay"></a>
### AmountLeftToPay
Determines the amount left to pay after voucher is applied.

{% raw %}
```liquid
{{ ApplyVoucherResult.AmountLeftToPay }}

```
{% endraw %}

Data Type: decimal

---

<a name="paymentcoveredbyvouchers"></a>
### PaymentCoveredByVouchers
Determines if a payment is covered by voucher.

{% raw %}
```liquid
{{ ApplyVoucherResult.PaymentCoveredByVouchers }}

```
{% endraw %}

Data Type: boolean

---

<a name="vouchercodealreadyredeemed"></a>
### VoucherCodeAlreadyRedeemed
True if the voucher code has already been redeemed.

{% raw %}
```liquid
{{ ApplyVoucherResult.VoucherCodeAlreadyRedeemed }}

```
{% endraw %}

Data Type: boolean

---

<a name="vouchercodealreadyregistered"></a>
### VoucherCodeAlreadyRegistered
True if the voucher code has already been registered.

{% raw %}
```liquid
{{ ApplyVoucherResult.VoucherCodeAlreadyRegistered }}

```
{% endraw %}

Data Type: boolean

---

<a name="vouchercodeexpired"></a>
### VoucherCodeExpired
True if the voucher code has expired.

{% raw %}
```liquid
{{ ApplyVoucherResult.VoucherCodeExpired }}

```
{% endraw %}

Data Type: boolean

---

<a name="vouchercodeinvalid"></a>
### VoucherCodeInvalid
True if the voucher code is invalid.

{% raw %}
```liquid
{{ ApplyVoucherResult.VoucherCodeInvalid }}

```
{% endraw %}

Data Type: boolean

---

<a name="vouchercodenotfound"></a>
### VoucherCodeNotFound
True if the voucher code wasn't found.

{% raw %}
```liquid
{{ ApplyVoucherResult.VoucherCodeNotFound }}

```
{% endraw %}

Data Type: boolean

---

<a name="vouchers"></a>
### Vouchers
The vouchers applied to the basket.

{% raw %}
```liquid
{{ ApplyVoucherResult.Vouchers }}

```
{% endraw %}

Data Type: Voucher Model

__Link to the voucher model__

---		