---
layout: collection
title: Blueprints
permalink: /blueprints/
---

**Blueprints** have been created to help you build your ecommerce website faster. We've done the hard work in creating as many code blocks as possible so that you do not have to.

Here's a list of the blueprints:

{% for bp in site.blueprints %}
  * **<a href="{{ bp.name}}">{{ bp.title }}</a>**
  {{ bp.description }}
{% endfor %}