---
layout: collection
title: PromotionResult
name: promotionresult
description: The result of trying to apply a promotion code to a shopping basket. Indicates whether the provided promotion code is valid as well as the promotion code that was applied/not applied.
 
---

## PromotionResult

* [PromotionCode](#promotioncode)
* [RemovedPromotionCode](#removedpromotioncode)
* [ValidPromotionCode](#validpromotioncode)

---

<a name="promotioncode"></a>
### PromotionCode
Determines the promotion code to apply to the shopping basket.

{% raw %}
```liquid
{{ PromotionResult.PromotionCode }}

```
{% endraw %}

Data Type: string

---

<a name="removedpromotioncode"></a>
### RemovedPromotionCode
Will be true if the promotion code is being removed.

{% raw %}
```liquid
{{ PromotionResult.RemovedPromotionCode }}

```
{% endraw %}

Data Type: boolean

---

<a name="validpromotioncode"></a>
### ValidPromotionCode
Will be true if the promotion code is valid.

{% raw %}
```liquid
{{ PromotionResult.RemovedPromotionCode }}

```
{% endraw %}

Data Type: boolean

---