---
layout: training
title: Syntax
name: Syntax
description: Introduction to the Liquid Syntax
---

## Syntax

* [Tags](#tags)
* [Models](#models)
* [Filters](#filters)

Liquid is a templating language that uses special markup (Tags, Models) that once rendered are replaced with content from the system.

<a name="tags"></a>
**Tags**

Tags make up the programming logic that tells templates what to do. Tags are identified by curly braces and percent signs: {% raw %}```{% tag %}```{% endraw %}.

The markup used in tags does not produce any visible text. This means that you can assign variables and create conditions and loops without showing any of the Liquid logic on the page.

{% raw %}
```liquid
{% if morning %}
  Coffee
{% endif %}
```
{% endraw %}

<a name="models"></a>
**Models**

Models (also known as Objects) are used to tell Liquid where to show content on a page. Models are identified by using curly brackets {{ and }}.

{% raw %}
```liquid
{{ Product.Description }}
```
{% endraw %}

<a name="filters"></a>
**Filters**

Filters allow you to modify the output of the model data. A filter is is added to data by adding a pipe and then the relevant filter name and value if required.

{% raw %}
```liquid
{{ Product.Description | Downcase }}
```
{% endraw %}