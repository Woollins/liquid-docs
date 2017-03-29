---
layout: collection
title: Pagination
name: paging
description: Blueprint for a typical listing pagingation.
---

**Pagination**

<div class="example-title">Input</div>
{% raw %}
```liquid
<!-- Display Number of Pages here -->
<span class="pages">
    {{ Navigation.Paging.NumberOfRows }} items
</span>

<!-- Main Pagination Section -->
<div class="pagesCont">
    <ul class="paging-section" data-max-pages="{{maxPages}}" data-previous-pages="{{previousPages}}" data-next-pages="{{nextPages}}">
    	<!-- if there are more than 1 page display pagination numbers / links -->
        {% if Navigation.Paging.NumberOfPages > 1 %}
            <li class="first" data-button-text="First">
            	<!-- if current page number is more than 1 display link to first page -->
                {% if Navigation.Paging.PageNumber > 1 %}
                    <button type="submit" data-option="product" data-page-number="1" class="tiny secondary button radius">First</button>
            	{% endif %}
            </li>
            <li class="prev" data-button-text='<i class="fa-angle-left fa"></i>'>
            	<!-- if current page number is more than 1 display link to previous page -->
                {% if Navigation.Paging.PageNumber > 1 %}
                    <button type="submit" data-option="product" data-page-number="{{Navigation.Paging.PageNumber | Minus: 1}}" class="button radius"><i class="fa-angle-left fa"></i></button>
                {% else %}
                    <span class="button-placeholder hide-for-medium"></span>
                {% endif %}
            </li>
            {% for i in (firstPage..lastPage) %}
            	<!-- display page numbers and links for each page -->
                <li class="{% if Navigation.Paging.PageNumber == i %}selected{% endif %}"><button type="submit" data-option="product" data-page-number="{{i}}" class="button radius page-number">{{i}}</button></li>
            {% endfor %}
            <li class="next" data-button-text='<i class="fa-angle-right fa"></i>'>
                {% if Navigation.Paging.PageNumber < lastPage %}
                	<!-- display link to next page if current page is not last page -->
                    <button type="submit" data-option="product" data-page-number="{{Navigation.Paging.PageNumber | Plus: 1}}" class="button radius"><i class="fa-angle-right fa"></i></button>
                {% endif %}
            </li>
            <li class="last" data-button-text="Last">
            	<!-- display link to last page if current page is not last page -->
                 {% if Navigation.Paging.PageNumber < lastPage %}
                    <button type="submit" data-option="product" data-page-number="{{Navigation.Paging.NumberOfPages}}" class="tiny secondary button radius">Last</button>
                {% endif %}
            </li>
        {% endif %}
    </ul>
    {% if Navigation.Paging.NumberOfPages > 1 %}
    <!-- display current page number and number of pages -->
    <label class="paging-info">Page {{ Navigation.Paging.PageNumber }} of {{Navigation.Paging.NumberOfPages}}</label>
    {% endif %}
</div>

```
{% endraw %}

<div class="example-title">Output</div>
{% raw %}
```html
<span class="pages">
	52 items
</span>
<div class="pagesCont">
	<ul class="paging-section" data-max-pages="5" data-previous-pages="2" data-next-pages="2">
		<li class="first" data-button-text="First">  </li>
		<li class="prev" data-button-text="<i class=&quot;fa-angle-left fa&quot;></i>"> 
			<span class="button-placeholder hide-for-medium"></span>  
		</li>  
		<li class="selected">
			<button type="submit" data-option="product" data-page-number="1" class="button radius page-number">1</button>
		</li>  
		<li class="">
			<button type="submit" data-option="product" data-page-number="2" class="button radius page-number">2</button>
		</li>  
		<li class="">
			<button type="submit" data-option="product" data-page-number="3" class="button radius page-number">3</button>
		</li>
		<li class="next" data-button-text="<i class=&quot;fa-angle-right fa&quot;></i>">
			<button type="submit" data-option="product" data-page-number="2" class="button radius"><i class="fa-angle-right fa"></i></button> 
		</li> <!--<li class="last" data-button-text="Last"> <button type="submit" data-option="product" data-page-number="3" class="tiny secondary button radius">Last</button>  </li>--> 
	</ul>  
	<label class="paging-info">Page 1 of 3</label></div>
</div>
```
{% endraw %}


