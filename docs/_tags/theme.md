---
layout: collection
title: Theme Tags
name: theme
description: A wide range of functions available
---

**Theme tags** have many functions, including:

* Outputting template-specific HTML markup
* Telling the theme which layout and snippets to use
* Splitting a returned array into multiple pages.

**Theme tags include**
* [comment](#comment)
* [include](#include)
* [schema](#shcema)
* [section](#section)

<a name="comment"></a>
### comment 
Allows you to leave un-rendered code inside a Liquid template. Any text within the opening and closing 'comment' blocks will not be output, and any Liquid code within will not be executed.
{% raw %}
```
This product is great {% comment %}, but expensive! {% endcomment %}.
```
{% endraw %}
Output: This product is great

---

<a name="include"></a>
### include 
Inserts a snippet from the snippets folder of a theme.
{% raw %}
```
{% include 'my-snippet-file' %}
```
{% endraw %}
You don't need to add the .liquid extension just the name of your snippet you want to include. When you include a snippet, the code inside it will have access to the variables within its parent template.

#### Including multiple variables in a snippet
There are two ways to include multiple variables in a snippet. You can assign and include them on different lines, which creates them in the parent template:
{% raw %}
```
{% assign my_variable = 'apples' %}
{% assign my_second_variable = 'oranges' %}
{% include 'snippet' %}
```
{% endraw %}
Or you can create variables on the same line where you include the snippet:
{% raw %}
```
{% include 'snippet', my_variable: 'apples', my_other_variable: 'oranges' %}
```
{% endraw %}

### include tag parameters

#### with - need to look at this bit again!
The with parameter assigns a value to a variable inside a snippet that shares the same name as the snippet.

For example, if you have a snippet named color.liquid which contains the following:
{% raw %}
color.liquid

color: '{{ color }}'
shape: '{{ shape }}'
{% endraw %}

Within theme.liquid, you can include the color.liquid snippet as follows:
{% raw %}
```
{% assign shape = 'circle' %}
{% include 'color' %}
{% include 'color' with 'red' %}
{% include 'color' with 'blue' %}
{% assign shape = 'square' %}
{% include 'color' with 'red' %}
```
{% endraw %}
Output:
color: '' shape: 'circle'
color: 'red' shape: 'circle'
color: 'blue' shape: 'circle'
color: 'red' shape: 'square'

---

<a name="schema"></a>
### schema 
The schema tag is used in section files to define the settings and properties of that section.
{% raw %}
```
{% schema %}
  {
    "name": "Header",
    "settings": [
      {
        "type": "image_picker",
        "id": "logo",
        "label": "Logo image"
      }
    ]
  }
{% endschema %}
```
{% endraw %}
The schema tags must contain valid JSON and cannot be nested inside another theme tag. You can read more about schema and section settings in the sections schema documentation.

---

<a name="section"></a>
### section 
Inserts a section from the sections folder of a theme.
{% raw %}
```
{% section 'header' %}
```
{% endraw %}
Output:
{% raw %}
``` html
<div id="shopify-section-header" class="shopify-section">
  <!-- content of sections/header.liquid -->
</div>
```
{% endraw %}
Including section files with the {% raw %}{% section %}{% raw %} tag will render a 'static' section. To learn more about sections and how to include them in your theme, check out the documentation on theme sections.
