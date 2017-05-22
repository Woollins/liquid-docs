---
layout: training
title: Training
permalink: /training/
description: Liquid training.
---

## Training

Intorduction to training section...

{% for lesson in site.training %}
  * **<a href="{{ site.baseurl }}{{ lesson.url }}">{{ lesson.title }}</a>**  
  {{ lesson.description }}
{% endfor %}