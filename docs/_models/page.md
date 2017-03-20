---
layout: collection
title: Page
name: page
description: Is used to access the metadata related to the page
---

## The Page Model

* [ApplyNoFollow](#applynofollow)
* [ApplyNoIndex](#applynoindex)
* [Links](#links)
* [MetaDescription](#metadescription)
* [MetaHeading](#metaheading)
* [MetaKeywords](#metakeywords)
* [Title](#title)
* [Url](#url)

---

<a name="applynofollow"></a>
### ApplyNoFollow 
Determines whether to apply the nofollow content property 

{% raw %}
```liquid
{{ Page.ApplyNoFollow }}
```
{% endraw %}

Data Type: string

---

<a name="applynoindex"></a>
### ApplyNoIndex 
Determines whether to apply the noindex content property 

{% raw %}
```liquid
{{ Page.ApplyNoIndex }}
```
{% endraw %}

Data Type: string

---

<a name="links"></a>
### Links 
Determines the html links that should be rendered for the page. 

{% raw %}
```liquid

```
{% endraw %}

Data Type: HtmlLink Model array

__need more detail on this__

---

<a name="metadescription"></a>
### MetaDescription
Determines the meta description of the page

{% raw %}
```liquid
{{ Page.MetaDescription }}
```
{% endraw %}

Data Type: string

---

<a name="metaheading"></a>
### MetaHeading
Determines the meta heading of the page

{% raw %}
```liquid
{{ Page.MetaHeading }}
```
{% endraw %}

Data Type: string

---

<a name="metakeywords"></a>
### MetaKeywords
Determines the meta keywords of the page

{% raw %}
```liquid
{{ Page.MetaKeywords }}
```
{% endraw %}

Data Type: string

---

<a name="title"></a>
### Title
Determines the title of the page

{% raw %}
```liquid
{{ Page.Title }}
```
{% endraw %}

Data Type: string

---

<a name="url"></a>
### Url
Determines the url of the page. This will be a relative url to the site root, e.g. /clothing/shirts/red-shirt_shirt1001

{% raw %}
```liquid
{{ Page.Url }}
```
{% endraw %}

Data Type: string

__need more detail on this__

---


