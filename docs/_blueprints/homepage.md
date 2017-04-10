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
    <!-- Optional full width slider code -->
{% endblock %}

{% block main %}
<section class="row home__prodRegion">
    <div class="medium-12 columns home__prodregion__title">
        <h1>Home Product Region</h1>
    </div>
    <!-- Check the product region exists -->
    {% if ProductRegion['HOME-PR1'] %}
        {% for prod in ProductRegion['HOME-PR1'].Products %}
            {% include 'SNIPPET-PRODUCT-REGION-HOME' %}
        {% endfor %}
    {% endif %}
</section>

<!-- Home call to action banners -->
<section class="row home__bannercalls">
    {{ ContentManagedRegion["HOME-CMR"].Segments["Banner1"].Contents | Prepend: '<article class="medium-4 columns homeBanners__CMR">' | Append: '</article>' }}
    {{ ContentManagedRegion["HOME-CMR"].Segments["Banner2"].Contents | Prepend: '<article class="medium-4 columns homeBanners__CMR">' | Append: '</article>' }}
    {{ ContentManagedRegion["HOME-CMR"].Segments["Banner3"].Contents | Prepend: '<article class="medium-4 columns homeBanners__CMR">' | Append: '</article>' }}
</section>

{% endblock %}

{% block page_scripts %}
<!-- Home specific slick scripts -->
{% endblock %}
```
{% endraw %}

---