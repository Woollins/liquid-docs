---
layout: collection
title: ProductSearchResult
name: productsearchresult
description: Contains the results of performing a product search.
 
---

## ProductSearchResult

* [Facets](#facets)
* [Products](#products)
* [SearchTerm](#searchterm)

---

<a name="facets"></a>
### Facets
Determines the Facets available to the search result. Only returned for EASearch.

{% raw %}
```liquid
{{ ProductSearchResult.Facets }}

```
{% endraw %}

Data Type: NavigationFacet Model

__link to NavigationFacet Model__

---

<a name="products"></a>
### Products
An array of products that were returned by the search, if any.

{% raw %}
```liquid
{{ ProductSearchResult.Products }}

```
{% endraw %}

Data Type: Product	Model

__link to Product	Model__

---

<a name="searchterm"></a>
### SearchTerm
Determines the search term used to find the products.

{% raw %}
```liquid
{{ ProductSearchResult.SearchTerm }}

```
{% endraw %}

Data Type: string

---