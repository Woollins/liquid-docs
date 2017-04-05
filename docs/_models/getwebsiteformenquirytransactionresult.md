---
layout: collection
title: GetWebsiteFormEnquiryTransactionResult
name: getwebsiteformenquirytransactionresult
description: Contains an array of Transaction Models and an array of Filter Models if any exist. 
 
---

## GetWebsiteFormEnquiryTransactionResult

* [Transactions](#transactions)
* [TransactionFilters](#transactionfilters)

---

<a name="transactions"></a>
### Transactions
The Transactions to display in a Website Form.

{% raw %}
```liquid
{{ GetWebsiteFormEnquiryTransactionResult.Transactions }}

```
{% endraw %}

Data Type: Transaction Model

__link to Transaction Model__

---

<a name="transactionfilters"></a>
### TransactionFilters
Used to filter the transactions.

{% raw %}
```liquid
{{ GetWebsiteFormEnquiryTransactionResult.TransactionFilters }}

```
{% endraw %}

Data Type: Filter Model

__link to Filter Model__

---