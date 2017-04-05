---
layout: collection
title: WebsiteCategory
name: websitecategory
description: Holds the website category information.
 
---

## WebsiteCategory

* [Category](#category)
* [CategoryUsageId](#categoryusageid)
* [Description](#description)
* [Required](#required)
* [SelectedCategoryId](#selectedcategoryid)

---

<a name="category"></a>
### Category
Determines the categories related to the parent Website Category.

{% raw %}
```liquid
{{ WebsiteCategory.Category }}

```
{% endraw %}

Data Type: Category Model

__link to the Category Model__

---

<a name="categoryusageid"></a>
### CategoryUsageId
Determines the Id of the Category Usage the Website Category belongs to.

{% raw %}
```liquid
{{ WebsiteCategory.CategoryUsageId }}

```
{% endraw %}

Data Type: int

---

<a name="description"></a>
### Description
Determines the Description of the Website Category.

{% raw %}
```liquid
{{ WebsiteCategory.Description }}

```
{% endraw %}

Data Type: string

---	

<a name="required"></a>
### Required
Determines whether or not selection of the Website Category is required.

{% raw %}
```liquid
{{ WebsiteCategory.Required }}

```
{% endraw %}

Data Type: boolean

---

<a name="selectedcategoryid"></a>
### SelectedCategoryId
Determines the Id of the currently selected category.

{% raw %}
```liquid
{{ WebsiteCategory.SelectedCategoryId }}

```
{% endraw %}

Data Type: int

---