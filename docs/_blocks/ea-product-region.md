---
layout: normal
title: EA Product Region
name: ea-product-region
description: a Selection of products, theses can be included within a carousel.
category: product
---

## EA Product Region
A Product Region is a selection of products that you want to inlude on a page.  For example you may want to include a Featured Products section on your homepage. Please see EA Product for product specific information.

<div class="example-title">HTML / Liquid</div>
{% raw %}
```liquid
<!-- To use the product region add in your regions code below - e.g. ProductRegion['CODE'] -->
{% assign PR = ProductRegion['HOME-PR1'] %}

<!-- Check the product region exists and has products -->
{% if PR.Products %}
<section data-component="ea-product-region" class="ea-product-region">
    <h2 class="ea-product-region__description">{{PR.Description}}</h2>
    <div class="row">
    {% for Product in PR.Products %}
        <!-- include the ea-product component -->
        <article class="ea-product small-6 medium-6 large-3 columns {% if forloop.last %}end{% endif %}" >
            {% include 'EA-PRODUCT' %}
        </article>
    {% endfor %}
    </div>
</section>
{% endif %}
```
{% endraw %}

<div class="example-title">SCSS</div>
{% raw %}
```scss
.ea-product-region{
	padding:2rem 0;

	// Product region description
	&__description{
		text-transform:uppercase;
		font-weight:bold;
		margin-bottom:1.5rem;
		text-align: center;
	}
}
```
{% endraw %}

__Also show this as a slider.__