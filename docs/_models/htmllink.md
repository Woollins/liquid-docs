---
layout: collection
title: HtmlLink
name: htmllink
description: Used to represent a HTML Link tag.
 
---

## HtmlLink

* [Relationship](#relationship)
* [Type](#type)
* [Url](#url)

---

<a name="relationship"></a>
### Relationship
The 'rel' attribute specifies the relationship between the current page and the linked item. For example, canonical, stylesheet, next, prev etc.

{% raw %}
```liquid
{{ HtmlLink.Relationship }}

```
{% endraw %}

Data Type: string

---

<a name="type"></a>
### Type
Defines the type of the link which is one of the Media Types such as 'text/css'.

{% raw %}
```liquid
{{ HtmlLink.Type }}

```
{% endraw %}

Data Type: string

---

<a name="url"></a>
### Url
Determines the 'href' attribute specifies the URL of the link to render.

{% raw %}
```liquid
{{ HtmlLink.Url }}

```
{% endraw %}

Data Type: string

---