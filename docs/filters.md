---
layout: collection
title: Filters
permalink: /filters/
---

Filters are simple methods that modify the output of numbers, strings, variables and objects. They are placed within an output tag {% raw %}**{{ }}**{% endraw %} and are denoted by a pipe character **{% raw %}`|`{% endraw %}**.

{% for filter in site.filters %}
  * **<a href="{{ filter.name}}">{{ filter.title }}</a>**
  {{ filter.description }}
{% endfor %}
