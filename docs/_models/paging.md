---
layout: collection
title: Paging
name: paging
description: Determines the paging criteria to be applied to a set of results.
 
---

## Paging

* [PageNumber](#pagenumber)
* [PageSize](#pagesize)
* [NumberOfPages](#numberofpages)
* [NumberOfRows](#numberofrows)
* [RemainingPages](#remainingpages)

---

<a name="pagenumber"></a>
### PageNumber
Determines the current page number.

{% raw %}
```liquid
{{ Navigation.Paging.PageNumber }}

```
{% endraw %}

Data Type: int

---

<a name="pagesize"></a>
### PageSize
Determines the current page size.

{% raw %}
```liquid
{{ Navigation.Paging.PageSize }}

```
{% endraw %}

Data Type: int

---

<a name="numberofpages"></a>
### NumberOfPages
Determines the total number of pages.

{% raw %}
```liquid
{{ Navigation.Paging.NumberOfPages }}

```
{% endraw %}

Data Type: int

---

<a name="numberofrows"></a>
### NumberOfRows
Determines the total number of rows.

{% raw %}
```liquid
{{ Navigation.Paging.NumberOfRows }}

```
{% endraw %}

Data Type: int

---

<a name="remainingpages"></a>
### RemainingPages
Determines the number of pages between the current PageNumber and the total number of pages.

{% raw %}
```liquid
{{ Navigation.Paging.RemainingPages }}

```
{% endraw %}

Data Type: int

---