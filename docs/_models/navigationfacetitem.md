---
layout: collection
title: NavigationFacetItem
name: navigationfacetitem
description: Represents a Navigation Facet Item contained within a particular Navigation Facet. e.g. A Facet of Colour would have a list of items like: Red, Green and Blue.
 
---

## NavigationFacetItem

* [Code](#code)
* [Count](#count)
* [Description](#description)
* [IsSelected](#isselected)


---

<a name="code"></a>
### Code
Determines the Facet Value or Code.

{% raw %}
```liquid
{{ NavigationFacetItem.Code }}

```
{% endraw %}

Data Type: string

---

<a name="count"></a>
### Count
Determines the total number of products for this Facet item.

{% raw %}
```liquid
{{ NavigationFacetItem.Count }}

```
{% endraw %}

Data Type: int

---

<a name="description"></a>
### Description
Determines the Facet item's description.

{% raw %}
```liquid
{{ NavigationFacetItem.Description }}

```
{% endraw %}

Data Type: string

---

<a name="isselected"></a>
### IsSelected
Determines whether this is the currently selected Facet item.

{% raw %}
```liquid
{{ NavigationFacetItem.IsSelected }}

```
{% endraw %}

Data Type: boolean

---