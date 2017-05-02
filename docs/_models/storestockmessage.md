---
layout: collection
title: StoreStockMessage
name: storestockmessage
description: Represents a Store Stock Message allowing a different "In Stock" message to be displayed per store. 
 
---

## StoreStockMessage

* [InStockMessage](#instockmessage)
* [StockStoreCode](#stockstorecode)
* [StockStoreDescription](#stockstoredescription)

---

<a name="instockmessage"></a>
### InStockMessage
Determines the In Stock Message to show for the associated store.

{% raw %}
```liquid
{{ StoreStockMessage.InStockMessage }}

```
{% endraw %}

Data Type: string

---

<a name="stockstorecode"></a>
### StockStoreCode
Determines the Code of the associated Stock Store.

{% raw %}
```liquid
{{ StoreStockMessage.StockStoreCode }}

```
{% endraw %}

Data Type: string

---

<a name="stockstoredescription"></a>
### StockStoreDescription
Determines the Description of the associated Stock Store.

{% raw %}
```liquid
{{ StoreStockMessage.StockStoreDescription }}

```
{% endraw %}

Data Type: string

---