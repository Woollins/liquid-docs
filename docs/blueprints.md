---
layout: collection
title: Blueprints
permalink: /blueprints/
---

**Blueprints** have been created to help you build your ecommerce website faster. We've done the hard work in creating as many code blocks as possible so that you do not have to.

Here's a list of the blueprints:

<div class="row">
	{% for bp in site.blueprints %}
	<div class="blueprint column medium-4">
		<div class="card" style="width: 300px;">
			<img src="http://placehold.it/300x150">
			<div class="card-section">
				<h4>{{ bp.title }}</h4>
				<p>{{ bp.description }}</p>
			</div>
			<a class="blueprint-link" href="{{ bp.name}}"></a>
		</div>
	  </div>
	{% endfor %}
</div>