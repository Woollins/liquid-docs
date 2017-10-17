---
layout: collection
title: Product Region
name: product-region
description: Blueprint for a product region.
---

**Product Region** is used to display a group of products defined within the system.

* [Basic](#basic)

---

<a name="basic"></a>
### Basic
Simple product region.

<div class="example-title">Input</div>
{% raw %}
```liquid
<!-- Check the product region exists -->
{% if ProductRegion['PROD-REGION-CODE'] %}
	<ul>
	<!-- Create a loop for all of the products -->
	{% for prod in ProductRegion['PROD-REGION-CODE'].Products %}
		<!-- Output a link and the description for each product -->
		<li><a href="{{ prod.NavigateUrl }}">{{ prod.Description }}</a></li>
	{% endfor %}
	</ul>
{% endif %}
```
{% endraw %}

<div class="example-title">Output</div>
{% raw %}
```html
<ul>
	<li><a href="/footwear/really-nice-trainers">Really nice trainers</a></li>
</ul>
```
{% endraw %}
