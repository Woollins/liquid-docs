---
layout: collection
title: Endpoint
permalink: /endpoint/
description: Endpoints are the way that all data is transferred between the web browser and the web server.
---

## Endpoints
A list of endpoints below:

{% for endpoint in site.endpoint %}
  * **<a href="{{ endpoint.name }}">{{ endpoint.title }}</a>**  
{% endfor %}