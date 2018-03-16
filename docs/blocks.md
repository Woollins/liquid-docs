---
layout: normal
title: Building Blocks
permalink: /blocks/
description: Building Blocks a library of componenets to help you build your site.
---

<div id="build">
	<div class="filter row">
		<div class="column medium-10">
			<ul id="options">
				<li data-value="all">
					<a href="#"><img src="../images/all.png" alt="all" /><span>All</span></a>
				</li>
				<li data-value="kits">
					<a href="#"><img src="../images/pages.png" alt="pages" /><span>Kits/Pages</span></a>
				</li>
				<li data-value="navigation">
					<a href="#"><img src="../images/navigation.png" alt="navigation" /><span>Navigation</span></a>
				</li>
				<li data-value="product">
					<a href="#"><img src="../images/product.png" alt="product" /><span>Product</span></a>
				</li>
				<li data-value="user">
					<a href="#"><img src="../images/user.png" alt="user" /><span>User/Account</span></a>
				</li>
				<li data-value="basket">
					<a href="#"><img src="../images/basket.png" alt="basket" /><span>Basket</span></a>
				</li>
				<li data-valuet="checkout">
					<a href="#"><img src="../images/checkout.png" alt="checkout" /><span>Checkout</span></a>
				</li>
				<li data-value="forms">
					<a href="#"><img src="../images/content.png" alt="content" /><span>Forms</span></a>
				</li>
				<li data-value="content">
					<a href="#"><img src="../images/content.png" alt="content" /><span>Content</span></a>
				</li>
			</ul>
		</div>
		<!-- class="search" automagically makes an input a search field. -->
		<div class="column medium-2">
			<input class="search" placeholder="Search" />
		</div>
	</div>

	<ul class="list">
	{% for bb in site.blocks %}
		<li class="{{ bb.category }} all">
			  	<a href="{{ bb.name }}">{{ bb.title }}</a>
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