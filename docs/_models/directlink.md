---
layout: collection
title: DirectLink
name: directlink
description: Provides access to the direct link properties.
 
---

## DirectLink

* [Code](#code)
* [Description](#description)
* [Parameter](#parameter)
* [Url](#url)

---

<a name="code"></a>
### Code
Stores the Code for the Direct Link.

{% raw %}
```liquid
{{ DirectLink.Code }}

```
{% endraw %}

Data Type: string

---

<a name="description"></a>
### Description
Stores the Description for this Direct Link. This will be the text displayed on the hyperlink.

{% raw %}
```liquid
{{ DirectLink.Description }}

```
{% endraw %}

Data Type: string

---

<a name="parameter"></a>
### Parameter
Stores any additional parameters to include in the link.

{% raw %}
```liquid
{{ DirectLink.Parameter }}

```
{% endraw %}

Data Type: string

---

<a name="url"></a>
### Url
Stores the URL for the page to launch on clicking this Direct Link.

{% raw %}
```liquid
{{ DirectLink.Url }}

```
{% endraw %}

Data Type: string

---