---
layout: collection
title: ContentManagedRegionSegment
name: contentmanagedregionsegment
description: Content Managed Regions can be broken up into one or more parts or segments. Each segment will provide access to its Name and Html Content.
 
---

## ContentManagedRegionSegment

* [Contents](#contents)
* [Elements](#elements)
* [Name](#name)

---

<a name="contents"></a>
### Contents
Determines the html/text content of the segment.

{% raw %}
```liquid
{{ ContentManagedRegion['HEADER'].Segments['LOGO'].Contents }}

```
{% endraw %}

Data Type: string

---

<a name="elements"></a>
### Elements
An array of ParameterParserElements. These either represent raw text or specific tokens that are converted to controls (labels or buttons).

{% raw %}
```liquid


```
{% endraw %}

Data Type: ParameterParserElement Model

__will need to link to ParameterParserElement Model / more info__

---

<a name="name"></a>
### Name
Determines the name of the segment.

{% raw %}
```liquid
{{ ContentManagedRegion['HEADER'].Segments.Name }}

```
{% endraw %}

Data Type: string

---