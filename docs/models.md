---
layout: collection
title: Models
permalink: /models/
---

{% for model in site.models %}
  <a href="{{ model.name }}">{{ model.title }}</a>
{% endfor %}
