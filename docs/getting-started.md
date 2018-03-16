---
layout: normal
title: Getting Started
permalink: /getting-started/
description: Now that you know what Liquid is let's have a look at the key features and how they work.
---

## Tags

Tags make up the programming logic that tells templates what to do. Tags are identified by curly braces and percent signs: {% raw %}{% tag %}{% endraw %}.

The markup used in tags does not produce any visible text. This means that you can assign variables and create conditions and loops without showing any of the Liquid logic on the page.

In the below example we are controlling the output by using a simple if statement. If the answer to our question (if statement) is true we render the words "Hello", if it's false we won't render anything.

{% raw %}
```liquid
{% if user %}
  Hello
{% endif %} 
```
{% endraw %}


## Models

Models (also known as Objects) are used to tell Liquid where to show content on a page. Models are identified by using curly brackets. 

The example below will pull the relevant data from our shop and output it in place of the Liquid placeholder. 

{% raw %}
```liquid
{{ Product.Description }} 
```
{% endraw %}


## Filters

Filters are used to modify the output of strings, numbers, variables, and objects. Their purpose is to manipulate the data in some way so that it's format changes.  A filter is is added to data by adding a pipe and then the relevant filter name and value if required.

{% raw %}
```liquid
{{ Product.Description | Downcase }}
```
{% endraw %}


## Operators

Operators are used within logic tags to determine what the output will be.  For example if you want to output specific data for a shirt you could use the following,  
{% raw %}
```liquid
{% if product.type == "Shirt" %}
  This is a shirt.
{% endif %}
```
{% endraw %}


## Loops

Loops allow us to output the same piece of code a set number of times.

Below is an example of how we would display the products on a listing page, we are using a loop to output the product description and price of all products within a certain hierarchy. 

{% raw %}
```liquid
{% for Product in HierarchyNode.Products %}
    <h2>{{Product.Description}}</h2>
    <p>{{ Product.StandardOurPrice_VatInclusivePrice | Round:2  }}</p>
{% endfor %} 
```
{% endraw %}