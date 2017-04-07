---
layout: collection
title: Layout
name: layout
description: Blueprints for your sites layout
---

## Layout

* [Master Page](#master)
  * [Breadcrumb](#breadcrumb)
* [Header](#header)
  * [Off Canvas Menu](#offcanvas)
  * [Content Managed Region](#cmr)
  * [Hierarchy Navigation](#hierarchynav)
  * [Mini Basket](#minibasket)
  * [Search](#search)
  * [Sign In](#signin)
* [Footer](#footer)
  * [Recently Viewed](#recentlyviewed)
  * [Hierarchy Navigation](#hierarchynavfoot)
  * [Website Form](#websiteform)

<a name="master"></a>
### Master Page
A Master Page containes the main layout information for your site.  When creating your master page makde sure you have the 'type' set to Template.  You can create multiple template files for pages with different layouts e.g the homepage would probably need a different layout to the product listing page.

<div class="example-title">Input</div>
{% raw %}
```liquid
<!DOCTYPE html>
<html lang="en">
    <head>
        <!-- The following information could be included in a snippet-->
        <meta name="description" content="{{Page.MetaDescription}}">
        <meta name="keywords" content="{{Page.MetaKeywords}}">
        <meta http-equiv="Content-Type" content="text/html; charset=UTF-8"/>
        <meta name="format-detection" content="telephone=no">
        <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1.0"/>
        {% if Page.ApplyNoIndex and Page.ApplyNoFollow %}
            <meta name="robots" content="noindex, nofollow">
            {% elsif Page.ApplyNoIndex %}
            <meta name="robots" content="noindex">
            {% elsif Page.ApplyNoFollow %}
            <meta name="robots" content="nofollow">
        {% endif %}
        <title>{% if Page.Title %}{{Page.Title}} {{ Product.Description }}{% else %}Standard Website {% endif %} - Standard Website</title>
        <link rel="icon" type="image/x-icon" href="{{ Website.StaticContentUrl }}/favicon.ico" />
        <!-- CSS  -->
        <link href="{{ Website.StaticContentUrl }}/css/filename.css" rel="stylesheet" />
        {% block page_head_scripts %}<!-- Include any specific header scripts -->{%endblock%}  
        {% for link in Page.Links%}
             <link rel="{{link.Relationship}}" {% if link.Type %}type="{{link.Type}}"{% endif %} href="{{link.Url}}" />
        {% endfor %}
    </head>
    <body>
        <div class="off-canvas-wrapper">
            <div class="off-canvas-wrapper-inner" data-off-canvas-wrapper>
                <div class="off-canvas-content" data-off-canvas-content>
                    {% include 'SNIPPET-OFF-CANVAS' %}
                    <header>
                        {% include 'SNIPPET-HEADER' %}
                    </header>
                    {% block banner %}{% endblock %}
                    {% unless Page.Links == '/' %}
                        {% include 'SNIPPET-BREADCRUMB' %}
                    {% endunless  %}
                    {% block title %}{% endblock %}
                    {% block main %}{% endblock %}
                    <footer>
                        {% include 'SNIPPET-FOOTER' %}
                    </footer>
                 </div>
            </div>
        </div>
        {% capture minify %}
        {% endcapture %}{{ minify | StripNewlines | Replace:'     ','' | Replace:'    ','' | Replace:'  ',' '}}
        {% include 'SNIPPET-SCRIPTS' %}
        {% block page_scripts %}
        {% endblock %}
    </body>
</html>
```
{% endraw %}

---

<a name="breadcrumb"></a>
### Breadcrumb
The breadcrumb is used show a navigation trail for users clicking through your site.

<div class="example-title">Input</div>
{% raw %}
```liquid
<section class="breadcrumb show-for-medium">
    <div class="row">
        <div class="column">
            <nav aria-label="You are here:">
                <ul class="breadcrumbs">
                    <li><a href="{{Endpoints.HomePage.Url}}">Home</a></li>
                    {% for node in HierarchyNode.HierarchyPathNodes %}
                        {% if forloop.last %}    
                            {% if Product %}
                                <li><a href="{{node.NavigateUrl}}">{{node.HierarchyLevel.Description}}</a></li>  
                                <li><span class="show-for-sr">Currents: </span>{{ Product.Description }}</li>                            
                            {% else %}
                                <li><span class="show-for-sr">Current: </span>{{node.HierarchyLevel.Description}}{{node.ContentManagedPage.Description}} </li> 
                            {% endif %}                    
                        {% else %}
                            <li><a href="{{node.NavigateUrl}}">{{node.HierarchyLevel.Description}}</a></li> 
                        {% endif %}
                    {% endfor %}
                </ul>
            </nav>
        </div>
    </div>
</section>
{% for node in HierarchyNode.HierarchyPathNodes %}
    {% if forloop.last %}    
        {% if Product %}
        
            <section class="breadcrumb hide-for-medium">
                <div class="row">
                    <div class="column">
                        <nav aria-label="You are here:" role="navigation">
                            <ul class="breadcrumbs">
                                <li><a href="{{node.NavigateUrl}}">&lt; Return to {{node.HierarchyLevel.Description}}</a></li>  
                            </ul>
                        </nav>
                    </div>
                </div>
            </section>
        
        {% endif %}                    
    {% endif %}
{% endfor %}
```
{% endraw %}

---

<a name="header"></a>
### Header
The Header of a webiste generally contains the following elements.

__maybe include the structure of the header include file__

<a name="offcanvas"></a>
### Off Canvas Menu
The off canvas menu is a well established mobile pattern for navigation that can also be used to create a responsive sidebar. 

<div class="example-title">Input</div>
{% raw %}
```liquid
<aside class="off-canvas position-left" id="offCanvas" data-off-canvas>
    {% assign MainHierarchy = Hierarchy["MAIN-NAVIGATION"] %}
    {% if Hierarchy["MAIN-NAVIGATION"] %}
        <nav class="side-nav">
            <div class="row">
                <div>
                    <ul class="menu vertical">
                    {% for node in Hierarchy["MAIN-NAVIGATION"].HierarchyNodes %}
                        {% if node.HierarchyNodes %}
                            <li class="level1 Mega">
                                <a href="{{ node.NavigateUrl | Downcase }}">{{ node.HierarchyLevel.Description }}<span class="fa-chevron-right fa"></span></a>
                                <div class="dropdown-panel">
                                    <a href="" class="backPanel"><span class="fa-chevron-left fa"></span> Back </a>
                                    {% for panels in node.HierarchyNodes %}
                                        <div class="panel">
                                                <ul class="vertical">            
                                                    {% for child in panels.HierarchyNodes %}    
                                                        {% if child.DirectLink %}
                                                            <li><a href="{{ child.NavigateUrl | Downcase }}">{{ child.DirectLink.Description }}</a></li>                  
                                                        {% endif %}
                                                        {% if child.HierarchyLevel %}
                                                            <li><a href="{{ child.NavigateUrl | Downcase }}">{{ child.HierarchyLevel.Description }}</a></li>  
                                                        {% endif %}
                                                        {% if child.ContentManagedPage %}
                                                            <li><a href="{{ child.NavigateUrl | Downcase }}">{{ child.ContentManagedPage.Description }}</a></li> 
                                                        {% endif %}  
                                                        {% if child.ContentManagedRegion %}
                                                            <li>CMR</li> 
                                                        {% endif %}                                               
                                                    {%endfor%}
                                                </ul>                    
                                            </div>     
                                    {%endfor%}
                                </div>
                            </li>
                        {% else %}
                            {% if node.DirectLink %}
                                <li>
                                    <a href="{{ node.NavigateUrl | Downcase }}">{{ node.DirectLink.Description }}</a>
                                </li>                   
                            {% endif %}
                            {% if node.HierarchyLevel %}
                                <li>
                                    <a href="{{ node.NavigateUrl | Downcase }}">{{ node.HierarchyLevel.Description }}</a>
                                </li>
                            {% endif %}
                            {% if node.ContentManagedPage %}
                                <li>
                                    <a href="{{ node.NavigateUrl | Downcase }}">{{ node.ContentManagedPage.Description }}</a>
                                </li>
                            {% endif %}
                        {% endif %}
                    {% endfor %}
                    </ul>
                </div>
            </div>
        </nav>
    {% endif %}                 
</aside>

```
{% endraw %}

---

<a name="cmr"></a>
### Content Managed Region
Content Managed Regions are used for static content that can be updated via the Content Manage Region tab rather than having to edit the main website files.  

<div class="example-title">Input</div>
{% raw %}
```liquid
{{ ContentManagedRegion["HEADER"].Segments["LOGO"].Contents }}
```
{% endraw %}

---

<a name="hierarchynav"></a>
### Hierarchy Navigation
The main navigation of the site, display Hierarchy Descriptions, Direct Links, Content Managed Regions and panels. 

<div class="example-title">Input</div>
{% raw %}
```liquid
{% assign MainHierarchy = Hierarchy["MAIN-NAVIGATION"] %}
{% if Hierarchy["MAIN-NAVIGATION"] %}
<nav class="head-nav">
<div class="row">
    <div class="show-for-large medium-12 large-12 columns">
        <ul class="menu">
        {% for node in Hierarchy["MAIN-NAVIGATION"].HierarchyNodes %}
            {% if node.HierarchyNodes %}
                <li class="level1 {{ node.HierarchyLevel.Code }}">
                    <a href="{{ node.NavigateUrl | Downcase }}">{{ node.HierarchyLevel.Description }}</a>
                    <div class="dropdown-panel mega-menu">
                        {% for panels in node.HierarchyNodes %}
                            <div class="panel column {{ panels.HierarchyPanel.Description }}">
                            {{ panels.HierarchyPanel.Title | Prepend: "<span class='panel-title'>" | Append: "</span>" }}
                              <ul class="vertical">            
                                  {% for child in panels.HierarchyNodes %}    
                                      {% if child.DirectLink %}
                                          <li><a href="{{ child.NavigateUrl | Downcase }}">{{ child.DirectLink.Description }}</a></li>                  
                                      {% endif %}
                                      {% if child.HierarchyLevel %}
                                          <li><a href="{{ child.NavigateUrl | Downcase }}">{{ child.HierarchyLevel.Description }}</a></li>  
                                      {% endif %}
                                      {% if child.ContentManagedPage %}
                                          <li><a href="{{ child.NavigateUrl | Downcase }}">{{ child.ContentManagedPage.Description }}</a></li> 
                                      {% endif %}  
                                      {% if child.ContentManagedRegion %}
                                         <li>{{ ContentManagedRegion[child.ContentManagedRegion.Code].Contents }}</li>
                                      {% endif %} 
                                   {%endfor%}
                               </ul>                    
                           </div>
                        {%endfor%}
                    </div>
                </li>
            {% else %}
                {% if node.DirectLink %}
                    <li>
                        <a href="{{ node.NavigateUrl | Downcase }}">{{ node.DirectLink.Description }}</a>
                    </li>                   
                {% endif %}
                {% if node.HierarchyLevel %}
                    <li>
                        <a href="{{ node.NavigateUrl | Downcase }}">{{ node.HierarchyLevel.Description }}</a>
                    </li>
                {% endif %}
                {% if node.ContentManagedPage %}
                    <li>
                        <a href="{{ node.NavigateUrl | Downcase }}">{{ node.ContentManagedPage.Description }}</a>
                    </li>
                {% endif %}
                    
            {% endif %}
        {% endfor %}
    </ul>
</div>
</div>
</nav>
{% endif %} 
```
{% endraw %}

---

<a name="minibasket"></a>
### Mini Basket
Display a link to your basket with the number of items. A mini basket will displayed with a full list of items. 

<div class="example-title">Input</div>
{% raw %}
```liquid
{% if Basket.TransactionLines != null and Basket.TransactionLines.size > 0 %}
    <a href="/Basket" class="basketLink medium-2 columns">
        BASKET {{ Basket.TransactionHeader.TotalQuantity | Round : 0  }}
    </a>
    <div class="basket-pop">
        {% for line in Basket.TransactionLines %}
        <div id="{{line.Id}}" class="basket-item">
            <a href="{{line.Product.NavigateUrl}}" class="item-image">
                <object data="{{ Website.StaticContentUrl }}/p/xs/{{line.Product.CodeToUseInUrl}}/{{line.Product.CodeToUseInUrl}}.jpg" type="image/png">
                    <img id="{{line.Product.CodeToUseInUrl}}" src="{{ Website.StaticContentUrl }}/p/xs/not_found.jpg"  alt="{{line.Product.Description}}" />
                </object>
            </a>                                      
            <a href="{{line.Product.NavigateUrl}}" class="item-description">
                    <span class="basket-item-description">{{ line.Product.Description }}</span>
            </a>
            <span class="item-price">{{line.Price | Round : 2 | FormatCurrency  : ActiveCurrency}}</span>
            <div class="item-qty">
                {% include BASKET.UPDATE %}    
            </div>
            <span class="item-total">
                {{line.LineValueIncludingVat | Round : 2 | FormatCurrency  : ActiveCurrency  }}
            </span>
            {% include "MINI.BASKET.REMOVE" %}
        </div>
        {% endfor %}
        <div id="basket-totals">
            <span class="basket-qty">Items: {{ Basket.TransactionHeader.TotalQuantity | Round : 0  }}</span> 
            <span class="basket-total">Total: {{Basket.TransactionHeader.GoodsGrossRounded | Round: 2 | FormatCurrency  : ActiveCurrency}}</span>
        </div>
    </div>
{% else %}
    <div class="basket-header medium-2 columns basket-empty">
        BASKET 0
    </div>
{% endif %}
```
{% endraw %}

---

<a name="search"></a>
### Search
Allow users to search your site for a specific product by using the product description or product code.

<div class="example-title">Input</div>
{% raw %}
```liquid
<div id="search-bar">
    <form class="search-form" > 
       <input autocomplete="off" title="Numbers & letters only" id="search-text" class="search-text" pattern="[a-z\d\-]*" name="SearchTermParameterName" type="search" placeholder="Keyword or product code" />
       <button id="header-search-button" type="submit" class="search show-for-large">Search</button>
    </form>
</div>
```
{% endraw %}

---

<a name="signin"></a>
### Sign In
Allow users to search your site for a specific product by using the product description or product code.

<div class="example-title">Input</div>
{% raw %}
```liquid
{% if SignInDetails.SignedIn %}
    <span class="show-for-medium"><a href="{{Endpoints.AccountManagementPage.Url}}"><span>My Account</span></a></span>
    {% else %}
    <a href="{{Endpoints.SignIn.Url}}"><span class="show-for-medium">Sign In</span></a> 
{% endif %}
```
{% endraw %}

---

<a name="footer"></a>
### Footer
The Footer of a webiste generally contains the following elements.

__maybe include the structure of the footer include file__

<a name="recentlyviewed"></a>
### Recently Viewed
This will display all the recently viewed products that a user has been looked at.

<div class="example-title">Input</div>
{% raw %}
```liquid
<div id="recently-viewed-products-section" {%if RecentlyViewedProducts.Ids %}data-recently-viewed-product-ids="{%for id in RecentlyViewedProducts.Ids%}{%if forloop.last%}{{id}}{%else%}{{id}},{%endif%}{%endfor%}"{%endif%}>
</div>
```
{% endraw %}

---

<a name="hierarchynavfoot"></a>
### Hierarchy Navigation
The footer naviagtion is implemented in the same way of the main hierachy navigation.  The name of the Hierarchy will just need updating. 

<div class="example-title">Input</div>
{% raw %}
```liquid
{% assign MainHierarchy = Hierarchy["FOOTER-NAVIGATION"] %}
{% if Hierarchy["FOOTER-NAVIGATION"] %}
<nav class="foot-nav">
    <ul class="menu foot-menu">
        {% for node in MainHierarchy.HierarchyNodes %}
            {% if node.HierarchyNodes %}
                <li class="medium-4 columns level1">
                    <span class="title">{{ node.HierarchyLevel.Description }}</span>
                    <div class="dropdown-panel">
                        {% for panels in node.HierarchyNodes %}
                            <div class="panel">
                                    <ul class="vertical">            
                                        {% for child in panels.HierarchyNodes %}    
                                            {% if child.DirectLink %}
                                                <li><a href="{{ child.NavigateUrl | Downcase }}">{{ child.DirectLink.Description }}</a></li>                  
                                            {% endif %}
                                            {% if child.HierarchyLevel %}
                                                <li><a href="{{ child.NavigateUrl | Downcase }}">{{ child.HierarchyLevel.Description }}</a></li>  
                                            {% endif %}
                                            {% if child.ContentManagedPage %}
                                                <li><a href="{{ child.NavigateUrl | Downcase }}">{{ child.ContentManagedPage.Description }}</a></li> 
                                            {% endif %}  
                                            {% if child.ContentManagedRegion %}
                                                <li>CMR</li> 
                                            {% endif %}                                               
                                        {%endfor%}
                                    </ul>                    
                                </div>     
                        {%endfor%}
                    </div>
                </li>
            {% else %}
                {% if node.DirectLink %}
                    <li>
                        <a href="{{ node.NavigateUrl | Downcase }}">{{ node.DirectLink.Description }}</a>
                    </li>                   
                {% endif %}
                {% if node.HierarchyLevel %}
                    <li>
                        <a href="{{ node.NavigateUrl | Downcase }}">{{ node.HierarchyLevel.Description }}</a>
                    </li>
                {% endif %}
                {% if node.ContentManagedPage %}
                    <li>
                        <a href="{{ node.NavigateUrl | Downcase }}">{{ node.ContentManagedPage.Description }}</a>
                    </li>
                {% endif %}
                    
            {% endif %}
        {% endfor %}
    </ul>
</nav>
{% endif %}
```
{% endraw %}

---
  
<a name="websiteform"></a>
### Website Form
A newsletter form is generally used within the footer. 

<div class="example-title">Input</div>
{% raw %}
```liquid
{% assign NEWSLETTER = WebsiteForm["NEWSLETTER"] %}
<div class="website-form" data-websiteformcode="NEWSLETTER" data-url="{{NEWSLETTER | GenerateWebsiteFormEndpointUrlForDetails }}"></div>
```
{% endraw %}

You will then need to create a partial that will create all the form elements.

<div class="example-title">Input</div>
{% raw %}
```liquid
<form action="{{WebsiteFormRule.EndpointUrlForCreate}}" method="post" data-abide novalidate>
    <div data-abide-error class="alert callout" style="display: none;">
        <p><i class="fa-exclamation-triangle fa"></i> There are some errors in your form.</p>
    </div> 
    {% if RelatedDataGroup %}
        {% if Required %}
            Required
        {% endif %}
        <div class="website-form-related-data small-12 medium-12 columns">
            {% include 'RELATEDDATAGROUPINPUT' with RelatedDataGroup %}
        </div>
    {% endif %}
    {% if RelatedDataGroupForContact %}
        <div class="website-form-contact-related-data small-12 medium-12 columns">
            {% include 'RELATEDDATAGROUPINPUT' with RelatedDataGroupForContact %}
        </div>
    {% endif %}
    <div class="small-12 medium-12 columns submit">
        <input class="button" type="submit" value="Submit" />
    </div>
</form>
```
{% endraw %}

---