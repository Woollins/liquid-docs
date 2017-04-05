---
layout: collection
title: Product Listing Sort / Page Size Options
name: sort-options
description: Blueprint for a typical listing sort options.
---

**Pagination**

<div class="example-title">Input</div>
{% raw %}
```liquid
<select id="page-size" data-page-size>
    <option id="0" value="">Page Size</option>
    <option id="2" value="12" {% if Navigation.Paging.PageSize == 12 %}selected{% endif %}>12</option>
    <option id="4" value="24" {% if Navigation.Paging.PageSize == 24 %}selected{% endif %}>24</option>
    <option id="12" value="36" {% if Navigation.Paging.PageSize == 36 %}selected{% endif %}>36</option>
    <option id="ALL" value="900" {% if Navigation.Paging.PageSize == 900 %}selected{% endif %}>ALL</option>
</select>
<select class="product-listing-sort-selection">
    <option>Sort By</option>
    {% for sortOption in Navigation.SortOptions %}
    <option value="{{ sortOption.ColumnName }}">{{ sortOption.ColumnDescription }}</option>
    {% endfor %}
</select>  
```
{% endraw %}
