---
layout: collection
title: Control Flow Tags
name: control-flow
description: create conditions that decide whether blocks of Liquid code get executed
---

**Control flow tags**
Control flow tags create conditions that decide whether blocks of Liquid code get executed.
* [if](#if)
* [unless](#unless)
* [else/elsif](#else/elseif)
* [case/when](#case/when)
* [Multiple conditions (and/or)](#multiple)


## Control flow tags

<a name="if"></a>
### if 
Executes a block of code if the result is true.
{% raw %}
```liquid
{% if product.Title == 'Nikon Camera' %}
  This Nikon Camera is great!
{% endif %}
```
{% endraw %}
Output: This Nikon Camera is great!

---

<a name="unless"></a>
### unless 
Like if, but only executes a block of code if the result is false.
{% raw %}
```liquid
{% unless product.Title == 'Nikon Camera' %}
  You are not buying a Nikon Camera
{% endunless %}
```
{% endraw %}
Output: You are not buying awesome shoes.

This is the same as using the following if statement,
{% raw %}
```liquid
{% if product.Title != 'Nikon Camera' %}
  You are not buying a Nikon Camera.
{% endif %}
```
{% endraw %}

---

<a name="else/else"></a>
### else/else if 
Executes a block of code if the result is true and another block of code if false.
{% raw %}
```liquid
{% if product.Title == 'Nikon Camera' %}
  You're shipping internationally. Your order should arrive in 2–3 weeks.
{% elsif product.Title == 'Canon Camera' %}
  Your order should arrive in 3–4 days.
{% else %}
  You are not buying a Nikon or Canon Camera.
{% endif %}
```
{% endraw %}

---

<a name="case/when"></a>
### case/when 
Creates a switch statement to execute a particular block of code when a variable has a specified value. 'case' initializes the switch statement, and 'when' statements define the various conditions.

You can optionally add an else statement at the end of the case to provide code to execute if none of the conditions are met.
{% raw %}
```liquid
{% case shipping_method.title %}
  {% when 'International Shipping' %}
     You're shipping internationally. Your order should arrive in 2–3 weeks.
  {% when 'Domestic Shipping' %}
    Your order should arrive in 3–4 days.
  {% when 'Local Pick-Up' %}
    Your order will be ready for pick-up tomorrow.
  {% else %}
     Thank you for your order!
{% endcase %}
```
{% endraw %}

---

<a name="multiple"></a>
### Multiple conditions (and/or) 
You can use 'and/or' to include one or more conditions within your tags.  If you use both 'and' and 'or' the 'and' operators will be evaluated first.

#### and
A condition with an 'and' will only be true if both the left and the right side of the condition are true.
{% raw %}
```liquid 
{% if product.Title == 'Nikon Camera' and product.Description == 'This camera is great!' %}
  You are buying a great Nikon Camera!
{% endif %}
```
{% endraw %}
If both conditions are true you will get the following message, 'You are buying a great Nikon Camera!'' 

#### or
A condition with an 'or' will be true if either the left or the right side of the condition is true.
{% raw %}
```liquid 
{% if product.Title contains 'SALE' or product.Description contains 'mycompany.com' %}
  Welcome! We're pleased to offer you a special discount of 15% on all products.
{% else %}
  Welcome to our store!
{% endif %}
``` 
{% endraw %}

