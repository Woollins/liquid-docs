---
layout: collection
title: ProductCollection
name: productcollection
description: Represents the Product Collection of specific collection product id.
 
---

## ProductCollection

* [ProductIdForCollection](#productidforcollection)
* [Products](#products)

---

<a name="productidforcollection"></a>
### ProductIdForCollection
Determines the main Product id of the product collection.

{% raw %}
```liquid
{{ ProductCollection.ProductIdForCollection }}

```
{% endraw %}

Data Type: int

---

<a name="products"></a>
### Products
Determines the products in this collection.

{% raw %}
```liquid
{{ ProductCollection.Products }}

```
{% endraw %}

Data Type: Product Model

__link to the Product Model__

---