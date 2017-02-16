---
layout: home
title: Getting Started
permalink: /getting-started/
---

Now that you have a know what Liquid is let's have a look at four key features and how they work in relation to theme development.

## Objects

Objects are used to tell Liquid where to show content on a page. Objects are identified by using curly brackets {% raw %}`{{`{% endraw %} and {% raw %}`}}`{% endraw %}.

{% raw %}
``` 
{{ Product.Title }}
{{ Product.Description }} 
```
{% endraw %}


The above examples will pull the relevant data from our shop and output it in place of the Liquid placeholder. 

{% raw %}```{{ Product.Title }}```{% endraw %} would display the title of the product, for example 'Nikon Camera' and  {% raw %}```{{ Product.Description }}```{% endraw %} will display the description of that product 'One of the best camera's around!'.

To summarise, Liquid output is very much like 'find and replace'. When rendering the template 3ex.net will go and find all instances of Liquid output tags and replace them with the relevant data from your store.

You'll also notice from these examples that Liquid uses the dot syntax for accessing data. The item preceding the dot is the variable, whereas the item after it is an attribute of that variable. For example our product variable above has both a title and description attribute.


## Tags

Tags make up the programming logic that tells templates what to do. Tags are identified by curly braces and percent signs: {% raw %}`{%`{% endraw %} and {% raw %}`%}`{% endraw %}.

The markup used in tags does not produce any visible text. This means that you can assign variables and create conditions and loops without showing any of the Liquid logic on the page.

{% raw %}
``` 
{% if user %}
  Hello
{% endif %} 
```
{% endraw %}

In the above example we are controlling the output by using a simple if statement. If the answer to our question (if statement) is true we render the words "Hello", if it's false we won't render anything.


Liquid tags allow us to control the flow of a template. For example we can highlight when a user is logged in. 

{% raw %}
```
{% if SignInDetails.SignedIn %}
    Customer is signed in
{% else %}
  Customer is not signed in
{% endif %}
```
{% endraw %}

In the above example we are controlling what the output to our template is using a simple if, else, endif statement. In many ways if statements are like questions.

In the above example if the answer to our if statement question is true we render the words 'Customer is signed in', if it's false our template carries on and outputs the text following our {% raw %}```{% else %}```{% endraw %} clause - in this case 'Customer is not signed in'.

*__You can view a full list of tags [here](Tags)__*

## Filters

Filters are used to modify the output of strings, numbers, variables, and objects. Their purpose is to manipulate the data in some way so that it's format changes. 

{% raw %}
``` 
{{ product.Description | Append: " (SALE!)" }}
```
{% endraw %}

The above would output 'Nikon Camera (SALE!)', without the filter the '(SALE!)' text would not be added.

*__You can view a full list of filters [here](Filters)__*

### Operators

Operators are used within logic tags to determine what the output will be.  For example if you want to output specific data for a shirt you could use the following,  
{% raw %}
```
{% if product.type == "Shirt" %}
  This is a shirt.
{% endif %}
```
{% endraw %}

In the above example we are saying if the product type is a shirt then output 'This is a Shirt'. If the statement is false then there won't be anything returned. 

Multiple operators can also be used,

{% raw %}
```
{% if product.type == "Shirt" or product.type == "Shoes" %}
  This is a shirt or a shoe.
{% endif %}
```
{% endraw %}

You have access to a wide range of operators in Liquid, many of which you will find yourself using regularly:

```==``` equal
```!=``` not equal
```>``` greater than
```<``` less than
```>=``` bigger or equal
```<=``` less or equal
```or``` this or that
```and``` must be this and that
```contains``` includes the substring if used on a string, or element if used on an array

*__Maybe link to a page with a full list and [explanations](https://help.shopify.com/themes/liquid/basics/operators)__*

### Loops

Loops allow us to output the same piece of code a set number of times.

{% raw %}
```
{% for Product in HierarchyNode.Products %}
    <h2>{{Product.Description}}</h2>
    <p>{{ Product.StandardOurPrice_VatInclusivePrice | Round:2  }}</p>
{% endfor %} 
```
{% endraw %}

This is an example of how we would display the products on a listing page, we are using a loop to output the product description and price of all products within a certain hierarchy. 

In the first line of the example above we are saying 'for Product' to determine the current item in the loop. Each time we go round our loop 'Product' will give us access to the data associated with each Product in turn.

The hierarchy level or category the product is in is defined by using the term 'HierarchyNode'. In the example above we are returning all the products within the current hierarchy level/category the user is on. If we were in the hierarchy level Shoes we would see all the shoes listed within that category. 

It doesn't matter that we don't know how many shoes are listed in the category, when we reach the end of the loop the next part of the template will be rendered.

{% raw %}
```
<h2>{{Product.Description}}</h2>
<p>{{ Product.StandardOurPrice_VatInclusivePrice  }}</p>
```
{% endraw %}

This part of our code is part HTML and part Liquid.  Within the '<h2>'' we are returning the description of the product. The second line will return the price of the product.

The final line of our example is our closing endfor statement. This effectively closes off any code that will be rendered within the loop.