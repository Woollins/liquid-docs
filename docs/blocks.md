---
layout: normal
title: Building Blocks
permalink: /blocks/
description: Building Blocks a library of componenets to help you build your site.
---

<div id="build">

	<!-- class="search" automagically makes an input a search field. -->
	<input class="search" placeholder="Search" />
	<!-- class="sort" automagically makes an element a sort buttons. The date-sort value decides what to sort by. -->
	<button class="sort" data-sort="all">All</button>
	<button class="sort" data-sort="kits">Kits/Pages</button>
	<button class="sort" data-sort="navigation">Navigation</button>
	<button class="sort" data-sort="product">Product</button>
	<button class="sort" data-sort="user">User/Account</button>
	<button class="sort" data-sort="basket">Basket</button>
	<button class="sort" data-sort="checkout">Checkout</button>
	<button class="sort" data-sort="forms">Forms</button>
	<button class="sort" data-sort="content">Content</button>

	<!--<ul>
		<li class="sort" data-sort="all">All</li>
		<li class="sort" data-sort="kits">Kits/Pages</li>
		<li class="sort" data-sort="navigation">Navigation</li>
		<li class="sort" data-sort="product">Product</li>
		<li class="sort" data-sort="user">User/Account</li>
		<li class="sort" data-sort="basket">Basket</li>
		<li class="sort" data-sort="checkout">Checkout</li>
		<li class="sort" data-sort="forms">Forms</li>
		<li class="sort" data-sort="content">Content</li>
	</ul>-->

	<ul class="list">
	{% for bb in site.blocks %}
		<li class="{{ bb.category }}">
	  	* **<a href="{{ bb.name }}">{{ bb.title }}</a>**  
	  	{{ bb.description }}   
	  	</li>
	{% endfor %}
	</ul>

	<script src="https://cdnjs.cloudflare.com/ajax/libs/list.js/1.5.0/list.min.js"></script>

	<script>
		var options = {
		  valueNames: [ 'all', 'kits', 'navigation', 'product', 'user', 'basket', 'checkout', 'forms', 'content' ]
		};

		var userList = new List('build', options);
	</script>

</div>