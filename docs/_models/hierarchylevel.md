---
layout: collection
title: HierarchyLevel
name: hierarchylevel
description: Used internally by the product model to determine what the type of product is. 
 
---

## HierarchyLevel

* [Code](#code)
* [Description](#description)
* [DescriptionToUseInUrl](#descriptiontouseinurl)
* [Id](#id)

---

<a name="code"></a>
### Code
Determines the hierachy level code.

{% raw %}
```liquid
{{ HierarchyLevel.Code }}

```
{% endraw %}

Data Type: string

---

<a name="description"></a>
### Description
Determines the hierachy level description.

{% raw %}
```liquid
{{ HierarchyLevel.Description }}

```
{% endraw %}

Data Type: string

---

<a name="descriptiontouseinurl"></a>
### DescriptionToUseInUrl
Similar to the Description, but with illegal URL characters removed to make it suitable for use in hyperlinks.

{% raw %}
```liquid
{{ HierarchyLevel.DescriptionToUseInUrl }}

```
{% endraw %}

Data Type: string

---

<a name="id"></a>
### Id
Unique identifier for looking up a particular hierarchy level.

{% raw %}
```liquid
{{ HierarchyLevel.Id}}

```
{% endraw %}

Data Type: int

---