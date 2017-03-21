---
layout: collection
title: Category
name: category
description: Provides access to the Category and it's attributes.
 
---

## Category

* [CategoryId](#categoryid)
* [CategoryUsageId](#categoryusageid)
* [Code](#code)
* [Description](#description)

---

<a name="categoryid"></a>
### CategoryId
Determines the Category Id

{% raw %}
```liquid
{{ Category.CategoryId }}

```
{% endraw %}

Data Type: int

---

<a name="categoryusageid"></a>
### CategoryUsageId
Determines the Id of the associated Category Usage Id.

{% raw %}
```liquid
{{ Category.CategoryUsageId }}

```
{% endraw %}

Data Type: int

---

<a name="code"></a>
### Code
Determines the Category's Code.

{% raw %}
```liquid
{{ Category.Code }}

```
{% endraw %}

Data Type: string

---

<a name="description"></a>
### Description
Determines the Category's Description.

{% raw %}
```liquid
{{ Category.Description }}

```
{% endraw %}

Data Type: string

---