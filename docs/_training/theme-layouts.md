---
layout: training
title: Theme Layouts
name: Theme Layouts
description: Introduction to theme layouts
---

## Theme Layouts

* [Templates](#templates) 
* [Physical Pages](#physical) 
* [Snippets](#snippets) 

<a name="templates"></a>
**Templates**

Template files are really powerful as they allow us to define all of the common elements of our website in one single file. The main benefit of templates is the ability to maintain and update one set of code, this makes them perfect for making global changes very quickly.

In order for us to allow pages to inherit these templates and inject page code we need to set up a a block that will act as a placeholder for the page content. 

Example template file:
<div class="example-title">Template: MASTER</div>
{% raw %}
```liquid
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Liquid training</title>
    </head>
    <body>
        <!--page content will be injected here from a matching block on the physical page file-->
        {% block main %}{% endblock %}
    </body>
</html>
```
{% endraw %}

<a name="physical"></a>
**Physical Pages**

These are the files you will be spending the most of your time working on. The physical pages contain all of the code required for each location of the website (home, hierarchy, listing, detail).
These pages are injected into the desired template with the following line of code that needs to be placed on line one of the physical page.

{% raw %}
```liquid
{% extends "MASTER" %}
```
{% endraw %}

Example physical page:

<div class="example-title">Physical page: HOME</div>
{% raw %}
```liquid
<!--this physical page is requesting to inherit the following template file-->
{% extends "MASTER" %}
<!--the following code will be injected into the matching block of the inherited template file-->
{% block main %}
    <h1>Hello world</h1>
{% endblock %}
```
{% endraw %}

<a name="snippets"></a>
**Snippets**

Snippets are files that contain reusable portions of code. The are really handy for inserting content that needs to be used in multiple locations with the ability to update the one file that can make a global change. A simple example would be to include a header or a footer into the template file.

Example of a snippet:

Step 1: Create the snippet file

<div class="example-title">Snippet: HEADER</div>
{% raw %}
```html
<div class="header">
    <img src="/img/logo.png"/>
</div>
```
{% endraw %}

Step 2: Add the snippet to a template/physical page

<div class="example-title">Template: MASTER</div>
{% raw %}
```liquid
<!--this will inject the HEADER snippet file-->
{{ include "header" }}
```
{% endraw %}