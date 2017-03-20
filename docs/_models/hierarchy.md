---
layout: collection
title: Hierarchy
name: hierarchy
description: The hierarchy is used to generate a menu structure allowing visitors to navigate the website. 
---

## Content Managed Page

* [Code](#code)
* [Description](#description)
* [DescriptionToUseInUrl](#descriptiontouseinurl)
* [HierarchyNodes](#hierarchynodes)
* [Id](#id)

---

<a name="code"></a>
### Code 
Displays the Hierarchy Code.

{% raw %}
```liquid
{{ Hierarchy.Code }}

{{ Hierarchy["SHOP"] }}

```
{% endraw %}

Data Type: string

---

<a name="description"></a>
### Description
Displays the Hierarchy Description.

{% raw %}
```liquid
{{ Hierarchy.Description }}

{{ Hierarchy["SHOP"].Description }}

```
{% endraw %}

Data Type: string

---

<a name="descriptiontouseinurl"></a>
### DescriptionToUseInUrl
Similar to the Description, but with illegal URL characters removed to make it suitable for use in hyperlinks.

{% raw %}
```liquid
{{ Hierarchy.DescriptionToUseInUrl }}

{{ Hierarchy["SHOP"].DescriptionToUseInUrl }}

```
{% endraw %}

Data Type: string

---

<a name="hierarchynodes"></a>
### HierarchyNodes
A collection of one or more hierarchy nodes that are used to generate the hierarchical structure.

{% raw %}
```liquid
{{ Hierarchy.HierarchyNodes }}

{{ Hierarchy["SHOP"].HierarchyNodes }}

```
{% endraw %}

Data Type: Hierarchy Node Model array

---

<a name="id"></a>
### Id
Unique identifier for looking up a particular hierarchy.

{% raw %}
```liquid
{{ Hierarchy.Id }}

{{ Hierarchy["SHOP"].Id }}

```
{% endraw %}

Data Type: int

---

__double check this__
		