---
layout: collection
title: Voucher
name: voucher
description: Provides information about a Voucher 
 
---

## Voucher

* [ExpiryDate](#expirydate)
* [RedeemedVoucherValue](#redeemedvouchervalue)
* [RemainingVoucherValue](#remainingvouchervalue)
* [VoucherCode](#vouchercode)
* [VoucherValue](#vouchervalue)

---

<a name="expirydate"></a>
### ExpiryDate
Determines the date upon which the voucher code will expire.

{% raw %}
```liquid
{{ Voucher.ExpiryDate }}

```
{% endraw %}

Data Type: DateTime

---

<a name="redeemedvouchervalue"></a>
### RedeemedVoucherValue
Determines the voucher amount that has been redeemed.

{% raw %}
```liquid
{{ Voucher.RedeemedVoucherValue }}

```
{% endraw %}

Data Type: decimal

---

<a name="remainingvouchervalue"></a>
### RemainingVoucherValue
Determines the voucher amount that remains.

{% raw %}
```liquid
{{ Voucher.RemainingVoucherValue }}

```
{% endraw %}

Data Type: decimal

---

<a name="vouchercode"></a>
### VoucherCode
Determines a 16 character voucher code.

{% raw %}
```liquid
{{ Voucher.VoucherCode }}

```
{% endraw %}

Data Type: string

---

<a name="vouchervalue"></a>
### VoucherValue
Determines the amount the voucher covers.

{% raw %}
```liquid
{{ Voucher.VoucherValue }}

```
{% endraw %}

Data Type: decimal

---