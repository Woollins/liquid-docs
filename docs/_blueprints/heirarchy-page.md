---
layout: collection
title: Heirarchy Page
name: heirarchy-page
description: Blueprint for a typical heirarchy page.
---

**Heirarchy**

<div class="example-title">Input</div>
{% raw %}
```liquid
 {% for Node in HierarchyNode.HierarchyNodes %}
    {% if Node.HierarchyPanel %}
        {% for child in Node.HierarchyNodes %}    
            {% if child.DirectLink %}
                <a href="{{ child.NavigateUrl | Downcase }}">{{ child.DirectLink.Description }}</a>          
            {% endif %}
            {% if child.HierarchyLevel %}
                <article>
                    <a href="{{child.NavigateUrl}}">
                        <img src="{{ Website.StaticContentUrl }}/h/s/{{ child.HierarchyLevel.Code }}.jpg" alt="" onError="this.src='{{ Website.StaticContentUrl }}/h/s/not_found.jpg';" />
                        {{ child.HierarchyLevel.Description | Prepend: '<h2 class="hierarchy-level-description">' | Append: '</h2>' }}
                    </a>
               </article> 
            {% endif %}
            {% if child.ContentManagedPage %}
                <article>
                    <a href="{{child.NavigateUrl | Downcase}}">
                        <img src="{{ Website.StaticContentUrl }}/h/s/{{ child.HierarchyLevel.Code }}.jpg" alt="" onError="this.src='{{ Website.StaticContentUrl }}/h/s/not_found.jpg';" />
                        {{ child.ContentManagedPage.Description | Prepend: '<h2 class="hierarchy-level-description">' | Append: '</h2>' }}
                    </a>
                </article> 
            {% endif %}  
        {%endfor%}
    {% endif %}
    {% if node.HierarchyLevel %}
        <article>
            <a href="{{Node.NavigateUrl}}">
                <img src="{{ Website.StaticContentUrl }}/h/s/{{ Node.HierarchyLevel.Code }}.jpg" alt="" onError="this.src='{{ Website.StaticContentUrl }}/h/s/not_found.jpg';" />
                {{ Node.HierarchyLevel.Description | Prepend: '<h2 class="hierarchy-level-description">' | Append: '</h2>' }}
            </a>
        </article>
    {% endif %}
    {% if Node.DirectLink %}
        <a href="{{ Node.NavigateUrl | Downcase }}" class="CMP-link">{{ Node.DirectLink.Description }}</a>
    {% endif %}
    {% if Node.HierarchyLevel %}
        <article>
    	    <a href="{{Node.NavigateUrl}}">
                <img src="{{ Website.StaticContentUrl }}/h/s/{{ Node.HierarchyLevel.Code }}.jpg" alt="" onError="this.src='{{ Website.StaticContentUrl }}/h/s/not_found.jpg';" />
                {{ Node.HierarchyLevel.Description | Prepend: '<h2 class="hierarchy-level-description">' | Append: '</h2>' }}
            </a>
        </article>
    {% endif %}
    {% if Node.ContentManagedPage %}
        <article>
            <a  href="{{ Node.NavigateUrl | Downcase }}" class="CMP-link">
     	        <img src="{{ Website.StaticContentUrl }}/h/s/{{ Node.HierarchyLevel.Code }}.jpg" alt="" onError="this.src='{{ Website.StaticContentUrl }}/h/s/not_found.jpg';" />
                {{ Node.ContentManagedPage.Description  | Prepend: '<h2 class="hierarchy-level-description">' | Append: '</h2>'}}
            </a>
        </article>
    {% endif %}
{% endfor %}
```
{% endraw %}
