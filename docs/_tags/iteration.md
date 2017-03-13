---
layout: collection
title: Iteration Tags
name: iteration
description: repeatedly run blocks of code
---

**Iteration tags** repeatedly run blocks of code.
* [for](#for)
* [cycle](#cycle)
* [tablerow](#tablerow)


<a name="for"></a>
### for 
'for' or 'for loops' repeatedly execute a block of code.
{% raw %}
```liquid
{% for product in HierarchyNode.Products %}
  {{ product.Title }}
{% endfor %}
```
{% endraw %}
The above will output all the product titles for every product within the hierarchy/category you are on.

#### else
You can use 'else' within a 'for loop' to output data if the loop doesn't contain anything.  For example if a hierarchy/category doesn't have any products.
{% raw %}
```liquid
{% for product in HierarchyNode.Products %}
  {{ product.Title }}
{% else %}
  The category is empty.
{% endfor %}
```
{% endraw %}

#### break
You can use 'break' to stop the loop.
{% raw %}
```liquid
{% for i in (1..5) %}
  {% if i == 4 %}
    {% break %}
  {% else %}
    {{ i }}
  {% endif %}
{% endfor %}
```
{% endraw %}
Output: 1 2 3

#### continue
You can skip the current iteration by using the 'continue' tag.
{% raw %}
```liquid
{% for i in (1..5) %}
  {% if i == 4 %}
    {% continue %}
  {% else %}
    {{ i }}
  {% endif %}
{% endfor %}
```
{% endraw %}
Output: 1 2 3  5

### for tag parameters

#### limit
Exits the for loop at a specific index.
{% raw %}
```liquid
<!-- numbers = [1,2,3,4,5] -->
{% for item in numbers limit:2 %}
    {{ item }}
{% endfor %}
```
{% endraw %}
Output: 1 2

#### offset
Starts the for loop at a specific index.
{% raw %}
```liquid
<!-- numbers = [1,2,3,4,5] -->
{% for item in numbers offset:2 %}
    {{ item }}
{% endfor %}
```
{% endraw %}
Output: 3 4 5 6

#### range
Defines a range of numbers to loop through. You can define the range using both literal and variable values.
{% raw %}
```liquid
{% for i in (3..5) %}
  {{ i }}
{% endfor %}
```
{% endraw %}
Output: 3 4 5
{% raw %}
```liquid
{% assign my_limit = 4 %}
{% for i in (1..my_limit) %}
    {{ i }}
{% endfor %}
```
{% endraw %}
Output: 1 2 3 4

#### reversed
Reverses the order of the loop.
{% raw %}
```liquid
<!-- if array = [1,2,3,4,5,6] -->
{% for item in array reversed %}
  {{ item }}
{% endfor %}
```
{% endraw %}
Output: 6 5 4 3 2 1

---

<a name="cycle"></a>
### cycle 
Loops through a group of strings and outputs them in the order that they were passed as parameters. Each time 'cycle' is called, the next string that was passed as a parameter is output.

'cycle' must be used within a for loop block. We can use 'cycle' for:

* applying odd/even classes to rows in a table
* applying a unique class to the last product thumbnail in a row
* cycle tag parameters

cycle accepts a parameter called cycle group in cases where you need multiple cycle blocks in one template. If no name is supplied for the cycle group, then it is assumed that multiple calls with the same parameters are one group.

The example below shows why cycle groups are necessary when there are multiple instances of the cycle block.
{% raw %}
``` html
<ul>
  {% for product in collections.collection-1.products %}
    <li{% cycle ' style="clear:both;"', '', '', ' class="last"' %}>
      <a href="{{ product.url | within: collection }}">
        <img src="{{ product.featured_image.src | img_url: '240x' }}" alt="{{ product.featured_image.alt }}" />
      </a>
    </li>
  {% endfor %}
</ul>

<ul>
  {% for product in collections.collection-2.products %}
    <li{% cycle ' style="clear:both;"', '', '', ' class="last"' %}>
      <a href="{{ product.url | within: collection }}">
        <img src="{{ product.featured_image.src | img_url: '240x' }}" alt="{{ product.featured_image.alt }}" />
      </a>
    </li>
  {% endfor %}
</ul>
```
{% endraw %}

In the example above, if the first collection only has two products, the second collection loop will continue the cycle where the first one left off. This will result in this undesired output:
{% raw %}
``` html
<ul>
  <li style="clear:both"></li>
</ul>

<ul>
  <li></li>
  <li class="last"></li>
  <li style="clear:both"></li>
  <li></li>
</ul>
```
{% endraw %}
To avoid this, you can use a cycle group for each cycle block, as shown below:
{% raw %}
``` html
<ul>
{% for product in collections.collection-1.products %}
  <li{% cycle 'group1': ' style="clear:both;"', '', '', ' class="last"' %}>
    <a href="{{ product.url | within: collection }}">
      <img src="{{ product.featured_image.src | img_url: '240x' }}" alt="{{ product.featured_image.alt }}" />
    </a>
  </li>
{% endfor %}
</ul>

<ul>
{% for product in collections.collection-2.products %}
  <li{% cycle 'group2': ' style="clear:both;"', '', '', ' class="last"' %}>
    <a href="{{ product.url | within: collection }}">
      <img src="{{ product.featured_image.src | img_url: '240x' }}" alt="{{ product.featured_image.alt }}" />
    </a>
  </li>
{% endfor %}
</ul>
```
{% endraw %}
With the code above, the two cycle blocks are independent of each other. The result is shown below:
{% raw %}
``` html
<ul>
  <li style="clear:both"></li>
  <li></li>
</ul>
<!-- new cycle group starts! -->
<ul>
  <li style="clear:both"></li>
  <li></li>
  <li></li>
  <li class="last"></li>
</ul>
```
{% endraw %}

---

<a name="tablerow"></a>
### tablerow 
Generates rows for an HTML table. Must be wrapped in an opening {% raw %}<table>{% raw %} and closing {% raw %}</table>{% raw %} HTML tags. For a full list of attributes available within a tablerow loop, see tablerow (object).
{% raw %}
``` html
<table>
  {% tablerow product in collection.products %}
    {{ product.title }}
  {% endtablerow %}
</table>
```
{% endraw %}
Output:
{% raw %}
``` html
<table>
  <tr class="row1">
    <td class="col1">
      Cool Shirt
    </td>
    <td class="col2">
      Alien Poster
    </td>
    <td class="col3">
      Batman Poster
    </td>
    <td class="col4">
      Bullseye Shirt
    </td>
    <td class="col5">
      Another Classic Vinyl
    </td>
    <td class="col6">
      Awesome Jeans
    </td>
  </tr>
</table>
```
{% endraw %}

### tablerow tag parameters

#### cols
Defines how many columns the tables should have.
{% raw %}
``` html
<table>
  {% tablerow product in collection.products cols:2 %}
    {{ product.title }}
  {% endtablerow %}
</table>
```
{% endraw %}
Output:
{% raw %}
``` html 
<table>
  <tr class="row1">
    <td class="col1">
      Cool Shirt
    </td>
    <td class="col2">
      Alien Poster
    </td>
  </tr>
  <tr class="row2">
    <td class="col1">
      Batman Poster
    </td>
    <td class="col2">
      Bullseye Shirt
    </td>
  </tr>
  <tr class="row3">
    <td class="col1">
      Another Classic Vinyl
    </td>
    <td class="col2">
      Awesome Jeans
    </td>
  </tr>
</table>
```
{% endraw %}

#### limit
Exits the tablerow loop after a specific index.
{% raw %}
```liquid
{% tablerow product in collection.products cols:2 limit:3 %}
  {{ product.title }}
{% endtablerow %}
```
{% endraw %}

#### offset
Starts the tablerow loop at a specific index.
{% raw %}
```liquid
{% tablerow product in collection.products cols:2 offset:3 %}
  {{ product.title }}
{% endtablerow %}
```
{% endraw %}

#### range
Defines a range of numbers to loop through. The range can be defined by both literal and variable numbers.
{% raw %}
``` html
<table>
  {% tablerow i in (3..5) %}
    {{ i }}
  {% endtablerow %}
</table>

{% assign num = 4 %}
<table>
  {% tablerow i in (1..num) %}
    {{ i }}
  {% endtablerow %}
</table>
```
{% endraw %}

