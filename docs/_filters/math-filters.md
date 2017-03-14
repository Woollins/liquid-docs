---
layout: collection
title: Math Filters
name: math-filters
description: allow you to apply mathematical tasks
---

**Math Filters**
Math filters allow you to apply mathematical tasks.

* [DividedBy](#divideby)
* [Minus](#minus) 
* [Plus](#plus) 
* [Times](#times)

<a name="divideby"></a>
### DividedBy 
Division
{% raw %}
```liquid
{{ "40" | DividedBy: 20 }}
```
{% endraw %}
Output: '2'

<a name="minus"></a>
### Minus 
Subtraction
{% raw %}
```liquid
{{ "40" | Minus: 20 }}
```
{% endraw %}
Output: '20'

<a name="plus"></a>
### Plus 
Addition
{% raw %}
```liquid
{{ "40" | Minus: 20 }}
```
{% endraw %}
Output: '20'

<a name="times"></a>
### Times 
Multiplication
{% raw %}
```liquid
{{ "40" | Times: 20 }}
```
{% endraw %}
Otuput: '800'