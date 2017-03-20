---
layout: collection
title: Models
permalink: /models/
description: Models (also known as Objects) are used to tell Liquid where to show content on a page.
---

## Models
A list of models below:

{% for model in site.models %}
  * **<a href="{{ model.name }}">{{ model.title }}</a>**  
{% endfor %}

