---
layout: collection
title: RelatedDataHeading
name: relateddataheading
description: Represents a Related Data Group that acts as a container for Related Data Headings. 
 
---

## RelatedDataHeading

* [Id](#id)
* [Description](#description)
* [Elements](#elements)

---

<a name="id"></a>
### Id
Determines the Id of the row.

{% raw %}
```liquid
{{ RelatedDataHeading.Id }}

```
{% endraw %}

Data Type: int

---

<a name="description"></a>
### Description
Determines the Description of the heading

{% raw %}
```liquid
{{ RelatedDataHeading.Description }}

```
{% endraw %}

Data Type: string

---

<a name="elements"></a>
### Elements
Determines the elements that should be displayed for this Heading.

{% raw %}
```liquid
{{ RelatedDataHeading.Elements }}

```
{% endraw %}

Data Type: RelatedDataElement Model

__link to the RelatedDataElement Model__

---