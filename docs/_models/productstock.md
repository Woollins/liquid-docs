---
layout: collection
title: ProductStock
name: productstock
description: Provides additional details about a product with regards to stock that are not available through the standard Product model. This model can be used to provide the stock quantity of the product as well as stock messages and expected dispatch date. 
 
---

## ProductStock

* [AvailableStock](#availablestock)
* [ExpectedDispatchDate](#expecteddispatchdate)
* [ProductGroupIdForControllingStock](#productgroupidforcontrollingstock)
* [ProductId](#productid)
* [PurchaseRestriction](#purchaserestriction)
* [QuantityUnavailableStockMessage](#quantityunavailablestockmessage)
* [SortOrder](#sortorder)
* [StockMessage](#stockmessage)
* [StockStoreCode](#stockstorecode)
* [StockStoreDescription](#stockstoredescription)
* [StockStoreId](#stockstoreid)
* [StockStoreMessage](#stockstoremessage)

---

<a name="availablestock"></a>
### AvailableStock
Determines the available stock quantity of the product. May be null if the stock quantity is not known.

{% raw %}
```liquid
{{ ProductStock.AvailableStock }}

```
{% endraw %}

Data Type: decimal

---

<a name="expecteddispatchdate"></a>
### ExpectedDispatchDate
Where there is no stock available for a product, this property can be used to give an indication as to when the product is likely to come back into stock. May be null if the expected dispatch date is not known.

{% raw %}
```liquid
{{ ProductStock.ExpectedDispatchDate }}

```
{% endraw %}

Data Type: DateTime

---

<a name="productgroupidforcontrollingstock"></a>
### ProductGroupIdForControllingStock
Determines the id of a product group that is used for controlling stock. This id is used to match against the product group of one of the configured stock messages.

{% raw %}
```liquid
{{ ProductStock.ProductGroupIdForControllingStock }}

```
{% endraw %}

Data Type: int

---

<a name="productid"></a>
### ProductId
Determines the id of the product that the stock model belongs to.

{% raw %}
```liquid
{{ ProductStock.ProductId }}

```
{% endraw %}

Data Type: int

---

<a name="purchaserestriction"></a>
### PurchaseRestriction
A value (0-3) that determines what purchase restriction should be applied to the product where: 0 = Prevent purchase of products that are out of stock; 1 = Allow purchase of products that are out of stock; 2 = Allow purchase to exceed available stock, but prevent purchase when out of stock; 3 = Prevent purchase of products that are out of stock without an expected receipt date.

{% raw %}
```liquid
{{ ProductStock.PurchaseRestriction }}

```
{% endraw %}

Data Type: int

---

<a name="quantityunavailablestockmessage"></a>
### QuantityUnavailableStockMessage
Determines the value of the property set according to the configured the stock messages. It can be used to display a warning to the website visitor if they try to purchase more of product than is currently available.

{% raw %}
```liquid
{{ ProductStock.QuantityUnavailableStockMessage }}

```
{% endraw %}

Data Type: string

---

<a name="stockmessage"></a>
### StockMessage
The value of this property is caculated by comparing the quantity in stock to the stock message rules. It can be used to display information about the stock status of the product to the website visitor.

{% raw %}
```liquid
{{ ProductStock.StockMessage }}

```
{% endraw %}

Data Type: string

---

<a name="stockstorecode"></a>
### StockStoreCode
The code of the associated Stock Store.

{% raw %}
```liquid
{{ ProductStock.StockStoreCode }}

```
{% endraw %}

Data Type: string

---

<a name="stockstoredescription"></a>
### StockStoreDescription
The Description of the associated Stock Store.

{% raw %}
```liquid
{{ ProductStock.StockStoreDescription }}

```
{% endraw %}

Data Type: string

---

<a name="stockstoreid"></a>
### StockStoreId
The Id of the associated Stock Store.

{% raw %}
```liquid
{{ ProductStock.StockStoreId }}

```
{% endraw %}

Data Type: int

---

<a name="stockstoremessage"></a>
### StockStoreMessage
Determines the Stock Store message to display.

{% raw %}
```liquid
{{ ProductStock.StockStoreMessage }}

```
{% endraw %}

Data Type: string

---