---
layout: collection
title: ContentManagedRegion
name: contentmanagedregion
description: Access specific Content Managed Regions it's code, description and segments.
---

## Content Managed Page

* [Code](#code)
* [Description](#description)
* [Content](#content)
* [Elements](#elements)
* [Segments](#segments)

---

<a name="code"></a>
### Code 
Displays the Content Managed Region Code.

{% raw %}
```liquid
{{ ContentManagedRegion['HEADER'].Code }}
```
{% endraw %}

Data Type: string

---

<a name="description"></a>
### Description
Displays the Content Managed Region Description.

{% raw %}
```liquid
{{ ContentManagedRegion['HEADER'].Description }}
```
{% endraw %}

Data Type: string

---

<a name="content"></a>
### Contents
Displays the Content of the Content Managed Region.

{% raw %}
```liquid
{{ ContentManagedRegion['HEADER'].Contents }}
```
{% endraw %}

Data Type: string

__maybe check this__

---

<a name="elements"></a>
### Elements
An array of ParameterParserElements. These either represent raw text or specific tokens that are converted to controls (labels or buttons).

{% raw %}
```liquid
{{  }}
```
{% endraw %}

Data Type: Parameter Parser Element Model array

__maybe check this - this will need explaining__

---

<a name="segments"></a>
### Segments
This allows access to the content of the Content Managed Regions Segments.

{% raw %}
```liquid
{{ ContentManagedRegion['HEADER'].Segments['Logo'].Contents }}
```
{% endraw %}

Data Type: Content Managed Region Segment Model Dictionary

__will need a link to the http://wiki.exactabacus.com/Content_Managed_Region_Segment_Model __

---

	
