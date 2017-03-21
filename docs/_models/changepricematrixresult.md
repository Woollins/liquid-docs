---
layout: collection
title: ChangePriceMatrixResult
name: changepricematrixresult
description: The result of changing the select price matrix (horizontal)
 
---

## ChangePriceMatrixResult

* [TransactionHeaderCategoriesUpdated](#transactionheadercategoriesupdated)
* [WasSuccessful](#wassuccessful)

---

<a name="transactionheadercategoriesupdated"></a>
### TransactionHeaderCategoriesUpdated
Determines whether the transaction header categories for the price matrix and currency were updated.

{% raw %}
```liquid
{{ ChangePriceMatrixResult.TransactionHeaderCategoriesUpdated }}

```
{% endraw %}

Data Type: boolean

---

<a name="wassuccessful"></a>
### WasSuccessful
Determines whether the price matrix selection was successful.

{% raw %}
```liquid
{{ ChangePriceMatrixResult.WasSuccessful }}

```
{% endraw %}

Data Type: boolean

---