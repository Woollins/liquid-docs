---
layout: collection
title: LoyaltyPoints
name: loyaltypoints
description: Used to store loyalty points data.
 
---

## LoyaltyPoints

* [LoyaltyPointsBalance](#loyaltypointsbalance)
* [PointsToConvert](#pointstoconvert)
* [RemainingLoyaltyPoints](#remainingloyaltypoints)

---

<a name="loyaltypointsbalance"></a>
### LoyaltyPointsBalance
Determines the Loyalty points balance.

{% raw %}
```liquid
{{ LoyaltyPoints.LoyaltyPointsBalance }}

```
{% endraw %}

Data Type: int

---

<a name="pointstoconvert"></a>
### PointsToConvert
Determines the Points to convert.

{% raw %}
```liquid
{{ LoyaltyPoints.PointsToConvert }}

```
{% endraw %}

Data Type: int

---

<a name="remainingloyaltypoints"></a>
### RemainingLoyaltyPoints
Determines the Remaining loyalty points.

{% raw %}
```liquid
{{ LoyaltyPoints.RemainingLoyaltyPoints }}

```
{% endraw %}

Data Type: int

---