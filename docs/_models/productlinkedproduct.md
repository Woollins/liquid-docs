---
layout: collection
title: ProductLinkedProduct
name: productlinkedproduct
description: Stores the linked products for a main product using a specific link category.
 
---

## ProductLinkedProduct

* [CategoryCode](#categorycode)
* [CategoryId](#categoryid)
* [Products](#products)

---

<a name="categorycode"></a>
### CategoryCode
Determines the Code of the Category that these linked Products are for.

{% raw %}
```liquid
{{ ProductLinkedProduct.CategoryCode }}

```
{% endraw %}

Data Type: string

---

<a name="categoryid"></a>
### CategoryId
Determines the Id of the Linked Product Category that these linked products are for.

{% raw %}
```liquid
{{ ProductLinkedProduct.CategoryId }}

```
{% endraw %}

Data Type: int

---

<a name="products"></a>
### Products
Determines the Linked products within the model

{% raw %}
```liquid
{{ ProductLinkedProduct.Products }}

```
{% endraw %}

Data Type: Product Model

__link to the Product Model__

---
