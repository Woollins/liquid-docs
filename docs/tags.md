---
layout: collection
title: Tags
permalink: /tags/
---

{% for tag in site.tags %}
  <a href="{{ tag.name }}">{{ tag.title }}</a>
{% endfor %}
