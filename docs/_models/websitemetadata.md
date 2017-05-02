---
layout: collection
title: WebsiteMetadata
name: websitemetadata
description: Provides access to heading, title, description and keywords.
 
---

## WebsiteMetadata

* [ApplyNoFollow](#applynofollow)
* [ApplyNoIndex](#applynoindex)
* [Description](#description)
* [Heading](#heading)
* [Keywords](#keywords)
* [Title](#title)

---

<a name="applynofollow"></a>
### ApplyNoFollow
Determines whether to apply the nofollow content property.

{% raw %}
```liquid
{{ WebsiteMetadata.ApplyNoFollow }}

```
{% endraw %}

Data Type: boolean

---

<a name="applynoindex"></a>
### ApplyNoIndex
Determines whether to apply the noindex content property.

{% raw %}
```liquid
{{ WebsiteMetadata.ApplyNoIndex }}

```
{% endraw %}

Data Type: boolean

---

<a name="description"></a>
### Description
Determines the description to use on the page.

{% raw %}
```liquid
{{ WebsiteMetadata.Description }}

```
{% endraw %}

Data Type: string

---

<a name="heading"></a>
### Heading
Determines the heading to use on the page.

{% raw %}
```liquid
{{ WebsiteMetadata.Heading }}

```
{% endraw %}

Data Type: string

---

<a name="keywords"></a>
### Keywords
Determines the keywords to use on the page.

{% raw %}
```liquid
{{ WebsiteMetadata.Keywords }}

```
{% endraw %}

Data Type: string

---

<a name="title"></a>
### Title
Determines the title to use on the page.

{% raw %}
```liquid
{{ WebsiteMetadata.Title }}

```
{% endraw %}

Data Type: string

---