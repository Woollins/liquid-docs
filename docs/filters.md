---
layout: collection
title: Filters
permalink: /filters/
---

Filters are simple methods that modify the output of numbers, strings, variables and objects. They are placed within an output tag {{ }} and are denoted by a pipe character |.

Input
```
{% raw %}<!-- product.title = "Awesome Shoes" -->
{{ product.title | upcase }}{% endraw %}
```
Output

AWESOME SHOES
In the example above, product is the object, title is its attribute, and upcase is the filter being applied.

Some filters require a parameter to be passed.

Input
```
{% raw %}{{ product.title | remove: "Awesome" }}{% endraw %}
```
Output

Shoes
Multiple filters can be used on one output. They are applied from left to right.

Input
```
{% raw %}<!-- product.title = "Awesome Shoes" -->
{{ product.title | upcase | remove: "AWESOME"  }}{% endraw %}
```
Output

SHOES