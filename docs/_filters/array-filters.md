---
layout: collection
title: Array Filters
name: array-filters
description: Change the output of the arrays
---

## Array Filters

* [Join](#join) 
* [First](#first) 
* [Last](#last) 
* [Size](#size) 
* [Sort](#sort)
* [StripHtml](#striphtml)
* [StripNewlines](#stripnewlines)

<a name="join"></a>
### Join 
Combines the items in an array into a single string.
{% raw %}
```liquid
{{ product.Tags | Join: ", " }}
```
{% endraw %}
This will display all the tags assigned to a product and joing them with a comma.
Output: 'Tag1, Tag2, Tag3'

<a name="first"></a>
### First 
Returns the first item of an array.
{% raw %}
```liquid
<!-- product.tags = "sale", "mens", "womens", "awesome" -->
{{ product.tags | First }}
```
{% endraw %}
Output: 'sale'

<a name="last"></a>
### Last 
Returns the last item of an array.
{% raw %}
```liquid
<!-- product.tags = "sale", "mens", "womens", "awesome" -->
{{ product.tags | Last }}
```
{% endraw %}
Output: 'awesome'

<a name="size"></a>
### Size 
Returns the number of characters in a string or the number of items in an array. 
{% raw %}
```liquid
{{ "This sale is great." | Size }}
```
{% endraw %}
Output: '19'

<a name="sort"></a>
### Sort 
Sort elements of the array.
{% raw %}
```liquid
{% assign my_array = "zebra, octopus, giraffe, Sally Snake" %}
{{ my_array | Sort  }}
```
{% endraw %}
Output: 'Sally Snake, giraffe, octopus, zebra'

<a name="striphtml"></a>
### StripHtml 
Remove all HTML tags from a string
{% raw %}
```liquid
{{ "Have <em>you</em> seen my <strong>shoes</strong>?" | StripHtml }}
```
{% endraw %}
Output: 'Have you seen my shoes?'

<a name="stripnewlines"></a>
### StripNewlines 
Remove all newlines from the string

Product Sepecification: 2005, Hatchback,
59.000 miles, Manual,
1.6L, Diesel
{% raw %}
```liquid
{{ Product["Answer_SPECIFICATION"] | StripNewlines }}
```
{% endraw %}
Output: '2005, Hatchback, 59.000 miles, Manual, 1.6L, Diesel'