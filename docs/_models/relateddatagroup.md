---
layout: collection
title: RelatedDataGroup
name: relateddatagroup
description: Represents a Related Data Group that acts as a container for Related Data Headings. 
 
---

## RelatedDataGroup

* [Id](#id)
* [Headings](#headings)

---

<a name="id"></a>
### Id
Determines the Id of the row.

{% raw %}
```liquid
{{ RelatedDataGroup.Id }}

```
{% endraw %}

Data Type: int

---

<a name="headings"></a>
### Headings
Determines the Headings that should be displayed. 

{% raw %}
```liquid
{{ RelatedDataGroup.Headings }}

```
{% endraw %}

Data Type: RelatedDataHeading Model

__link to the RelatedDataHeading Model__

---