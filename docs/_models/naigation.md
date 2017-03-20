---
layout: collection
title: Navigation
name: navigation
description: The Navigation Model represents the data that can be used to manipulate page navigation. This includes sorting, paging and more.
 
---

## Navigation

* [Paging](#paging)
* [SortOptions](#sortoptions)
* [BaseUrl](#baseurl)
* [SelectedPageSize](#selectedpagesize)
* [SelectedSortColumnName](#selectedsortcolumnname)
* [ProductFilters](#productfilters)
* [SelectedFilterValue](#selectedfiltervalue)

---

<a name="paging"></a>
### Paging
Determines the paging for the current element. This would be used to display the paging for products.

{% raw %}
```liquid
{{ Navigation.Paging }}

```
{% endraw %}

Data Type: Paging Model

__provide link to paging model__

---

<a name="sortoptions"></a>
### SortOptions
Displays the available sort options.  

{% raw %}
```liquid
{{ Navigation.SortOptions }}

```
{% endraw %}

Data Type: Sort Option Model array

__provide link to Sort Option Model array__

---

<a name="baseurl"></a>
### BaseUrl
Determines the Url of the current page without any Navigation criteria applied.

{% raw %}
```liquid
{{ Navigation.BaseUrl }}

```
{% endraw %}

Data Type: string

---

<a name="selectedpagesize"></a>
### SelectedPageSize
Determines the currently selected page size.

{% raw %}
```liquid
{{ Navigation.SelectedPageSize }}

```
{% endraw %}

Data Type: int

__may need more info__

---

<a name="selectedsortcolumnname"></a>
### SelectedSortColumnName
Determines the name of the currently selected sort column. This would be used to select the relevent option when rendering the sort options.

{% raw %}
```liquid
{{ Navigation.SelectedSortColumnName }}

```
{% endraw %}

Data Type: string

__may need more info__

---

<a name="productfilters"></a>
### ProductFilters
Available filter products to restrict the items being displayed.

{% raw %}
```liquid
{{ Navigation.ProductFilters }}

```
{% endraw %}

Data Type: Product Filter Model array

__may need more info / link to Product Filter Model array__

---

<a name="selectedfiltervalue"></a>
### SelectedFilterValue
Determines the currently selected filter value.

{% raw %}
```liquid
{{ Navigation.SelectedFilterValue }}

```
{% endraw %}

Data Type: string

__may need more info__

---
	
		