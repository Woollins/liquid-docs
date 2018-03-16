---
layout: normal
title: EA Footer Navigation
name: ea-footer-navigation
description: A secondary navigational element.
category: navigation
---

## EA Footer Navigation
A way of navigating to any secondary/information pages, for example Terms & Condtions, About Us

<div class="example-title">HTML / Liquid</div>
{% raw %}
```liquid
<div class="footer-bottom__nav">
    {% for node in Hierarchy["FOOTER-NAVIGATION"].HierarchyNodes %}             
        {% if node.HierarchyPanel %}
        <div class="column small-12 medium-6 large-4">
                <h5>{{ node.HierarchyPanel.Title }}</h5>
                <ul>
                    {% for links in node.HierarchyNodes %}
                        {% if links.DirectLink %}
                            <li><a href="{{ links.NavigateUrl }}"><i class="fa fa-caret-right" aria-hidden="true"></i> {{ links.DirectLink.Description }}</a></li>                  
                        {% endif %}
                        {% if links.HierarchyLevel %}
                            <li><a href="{{ links.NavigateUrl }}"><i class="fa fa-caret-right" aria-hidden="true"></i> {{ links.HierarchyLevel.Description }}</a></li>  
                        {% endif %}
                        {% if links.ContentManagedPage %}
                            <li><a href="{{ links.NavigateUrl }}"><i class="fa fa-caret-right" aria-hidden="true"></i> {{ links.ContentManagedPage.Description }}</a></li> 
                        {% endif %} 
                    {% endfor %}
                </ul>
            </div>
        {% endif %}
    {% endfor %}            
</div>
{% endif %}
```
{% endraw %}

<div class="example-title">SCSS</div>
{% raw %}
```scss

```
{% endraw %}

__Include the SCSS__