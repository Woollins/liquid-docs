---
layout: collection
title: Home Page
name: homepage
description: Blueprint for creating a Home page
---

### Master Page

Create a new physical page and enter a name e.g. HOME

__need to base this on standard when complete__

<div class="example-title">HOME</div>
{% raw %}
```liquid
{% extends 'MASTER' %}
{% block banner %}
<!-- include a content managed region to  be able to pull through the slider images -->
{% endblock %}
{% block content %}
<!-- include content managed regions / product regions specific to the homepage -->
{% endblock %}
{% block page-scripts %}
<!-- include any page specific scripts -->
{% endblock %}
```
{% endraw %}