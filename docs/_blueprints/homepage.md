---
layout: collection
title: Home Page
name: homepage
description: Blueprint for creating a Home page
---

## Home Page

* [Home Page](#home)
  * [Content Managed Region - Slider](#cmr-slider)
  * [Product Region](#productregion)
  * [Latest from the Blog](#bloglatest)

<a name="home"></a>
### Home Page
The layout for the homepage is a physical page which consists of content managed regions and product regions.

<div class="example-title">Input</div>
{% raw %}
```liquid
{% extends "MASTER" %}
{% block page_head_scripts %}
{% endblock %} 
{% block banner %}
    <!-- include any banner if required -->
{% endblock %}

{% block main %}
    <!-- include any content blocks required -->
{% endblock %}

{% block page_scripts %}
    <!-- Home specific scripts -->
{% endblock %}
```
{% endraw %}

---

<a name="cmr-slider"></a>
### Content Managed Region - Slider
Create a Snippet for the Slider to be included on the homepage. This can contain multiple segments for banners.

<div class="example-title">Input</div>
{% raw %}
```liquid
<div class="banner_fullwidth">
    {% if ContentManagedRegion["HOME-SLIDER"].Segments["Slide 1"].Contents != "" %}
        <div class="slideBox">
            {{ ContentManagedRegion["HOME-SLIDER"].Segments["Slide 1 link"].Contents | Prepend: '<a href="' | Append: '">' }}
            {{ ContentManagedRegion["HOME-SLIDER"].Segments["Slide 1 image"].Contents }}
            </a>
        </div>
    {% endif %} 
    {% if ContentManagedRegion["HOME-SLIDER"].Segments["Slide 2"].Contents != "" %}
        <div class="slideBox">
            {{ ContentManagedRegion["HOME-SLIDER"].Segments["Slide 2 link"].Contents | Prepend: '<a href="' | Append: '">' }}
            {{ ContentManagedRegion["HOME-SLIDER"].Segments["Slide 2 image"].Contents }}
            </a>
        </div>
    {% endif %} 
    {% if ContentManagedRegion["HOME-SLIDER"].Segments["Slide 3"].Contents != "" %}
        <div class="slideBox">
            {{ ContentManagedRegion["HOME-SLIDER"].Segments["Slide 3 link"].Contents | Prepend: '<a href="' | Append: '">' }}
            {{ ContentManagedRegion["HOME-SLIDER"].Segments["Slide 3 image"].Contents }}
            </a>
        </div>
    {% endif %} 
    {% if ContentManagedRegion["HOME-SLIDER"].Segments["Slide 4"].Contents != "" %}
        <div class="slideBox">
            {{ ContentManagedRegion["HOME-SLIDER"].Segments["Slide 4 link"].Contents | Prepend: '<a href="' | Append: '">' }}
            {{ ContentManagedRegion["HOME-SLIDER"].Segments["Slide 4 image"].Contents }}
            </a>
        </div>
    {% endif %} 
    {% if ContentManagedRegion["HOME-SLIDER"].Segments["Slide 5"].Contents != "" %}
        <div class="slideBox">
            {{ ContentManagedRegion["HOME-SLIDER"].Segments["Slide 5 link"].Contents | Prepend: '<a href="' | Append: '">' }}
            {{ ContentManagedRegion["HOME-SLIDER"].Segments["Slide 5 image"].Contents }}
            </a>
        </div>
    {% endif %}    
</div>
```
{% endraw %}

---

<a name="productregion"></a>
### Product Region
Display a selection of Products within a Product Region.

<div class="example-title">Input</div>
{% raw %}
```liquid
<!-- Check if the Product Region exists if it does then loop through the products -->
<section class="row home__prodRegion">
    <div class="medium-12 columns home__prodregion__title">
        <h1>Home Product Region</h1>
    </div>
    {% if ProductRegion['HOME-PR1'] %}
        {% for prod in ProductRegion['HOME-PR1'].Products %}
            <div class="small-6 medium-3 column">
                <a href="{{product.NavigateUrl}}" class="prodImg" data-productId="{{ product.Id }}" data-productCode="{{ product.Code }}">
                  <img src="{{ Website.StaticContentUrl }}/p/m/{{ product.Code }}.jpg" alt="{{ product.Description }}" onerror="this.src='{{ Website.StaticContentUrl }}/p/m/not_found.jpg'">
                </a>
                <h3><a href="{{ product.NavigateUrl }}">{{ product.Description }}</a></h3>
                <p>£{{ product.StandardOurPrice_VatInclusivePrice | Round : 2}}</p>
            </div>
        {% endfor %}
    {% endif %}
</section>
```
{% endraw %}

---

<a name="bloglatest"></a>
### Latest from the Blog
Create a Snippet for the Slider to be included on the homepage. This can contain multiple segments for banners.

<div class="example-title">Input</div>
{% raw %}
```liquid
{% assign Blog = ProductRegion["RECENT-POSTS"] %}
{% if Blog.Products %}
    <section class="row home__blogRegion">
        <div class="medium-12 columns home__blogregion__title">
                <h2>Latest from the Blog</h2>
        </div>
        <div class="article-slider row">    
            {% for post in Blog.Products | limit:6 %}   
                <div class="small-6 medium-3 column">                
                    <img src="{{ Website.StaticContentUrl }}/img/b/s/{{ post.Code}}.jpg" onerror="this.src='{{ Website.StaticContentUrl }}/img/b/s/not_found.jpg'" alt="{{ post.Description }}">
                    <h3><a href="{{post.NavigateUrl}}">{{ post.Description }}</a></h3>
                    {% if post.Answer_BCSNIPPET %}
                        <p>{{ post.Answer_BCSNIPPET }}</p>
                    {% endif %}
                </div>
            {% endfor %}            
        </div>
    </section>
{% endif %}

```
{% endraw %}

---
