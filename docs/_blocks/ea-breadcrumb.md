---
layout: normal
title: EA Breadcrumb
name: ea-breadcrumb
description: Enhance the way users find their way around your webiste.
category: navigation
---

## EA Breadcrumb
They are an effective visual aid that indicates the location of the user within the website’s hierarchy, making it a great source of contextual information for landing pages.

<div class="example-title">HTML / Liquid</div>
{% raw %}
```liquid
<section class="row ea-breadcrumb show-for-medium">
    <nav aria-label="You are here:" class="column">
        <ul class="ea-breadcrumb__list">
            <li><a href="{{Endpoints.HomePage.Url}}">Home</a></li>
            {% for node in HierarchyNode.HierarchyPathNodes %}
                {% if forloop.last %}    
                    {% if Product %}
                        <li><i class="fa fa-caret-right" aria-hidden="true"></i></li>
                        <li><a href="{{node.NavigateUrl}}">{{node.HierarchyLevel.Description}}</a></li> 
                        <li><i class="fa fa-caret-right" aria-hidden="true"></i></li>
                        <li><span class="show-for-sr">Currents: </span>{{ Product.Description }}</li> 
                    {% else %}
                        <li><i class="fa fa-caret-right" aria-hidden="true"></i></li>
                        <li><span class="show-for-sr">Current: </span>{{node.HierarchyLevel.Description}}{{node.ContentManagedPage.Description}} </li> 
                    {% endif %}                    
                {% else %}
                    <li><i class="fa fa-caret-right" aria-hidden="true"></i></li>
                    <li><a href="{{node.NavigateUrl}}">{{node.HierarchyLevel.Description}}</a></li>
                {% endif %}
            {% endfor %}
        </ul>
    </nav>
</section>

{% for node in HierarchyNode.HierarchyPathNodes %}
    {% if forloop.last %}    
        {% if Product %}
            <section class="row ea-breadcrumb hide-for-medium">
                <nav class="column" aria-label="You are here:" role="navigation">
                    <ul class="ea-breadcrumb__list">
                        <li><a href="{{node.NavigateUrl}}">&lt; Return to {{node.HierarchyLevel.Description}}</a></li>  
                    </ul>
                </nav>
            </section>
        {% endif %}                    
    {% endif %}
{% endfor %}
```
{% endraw %}

<div class="example-title">SCSS</div>
{% raw %}
```scss

.ea-breadcrumb{
	&__list{
		margin: 1rem 0;
		list-style:none;
		font-size:0.9rem;
		li {
			display:inline-block;
			a {
				color: $primary-color;
			}
			&:not(:last-child)::after{
				content: '';
				margin: 0.4rem;
			}
		}
	}
}

```
{% endraw %}
