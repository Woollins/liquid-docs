---
layout: collection
title: Tags
permalink: /tags/
---

**Liquid tags** are the programming logic that tells templates what to do. Tags are wrapped in: {% raw %}**{% %}**{% endraw %} characters.

There are four main types of tags:

{% for tag in site.tags %}
  * **<a href="{{ tag.name}}">{{ tag.title }}</a>**
  {{ tag.description }}
{% endfor %}
