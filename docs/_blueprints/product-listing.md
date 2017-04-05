---
layout: collection
title: Product Listing
name: product-listing
description: Blueprint for a typical product listing page.
---

**Product Listing** Display a list of products applied to a hierarchy level.

* [Basic](#basic)
* [Advanced](#advanced)

### Product List Physical Page

<div class="example-title">Create a new physical page for product listing and add the following code.</div>
{% raw %}
```liquid
<section id="product-listing-section">
    {% include PARTIAL.PRODUCT-LISTING %}
</section>
```
{% endraw %}

<a name="basic"></a>
### Basic
Simple listing page.
Create a new snipped named "PARTIAL.PRODUCT-LISTING"

<div class="example-title">PARTIAL.PRODUCT-LISTING</div>
{% raw %}
```liquid
{% for Product in HierarchyNode.Products %}
<article itemscope itemtype="http://schema.org/Product">
    <a href="{{Product.NavigateUrl}}" class="product-image" data-productId="{{Product.Id}}" data-productCode="{{Product.Code}}">
        <img id="{{ Product.Code }}" src="{{ Website.StaticContentUrl }}/p/m/{{Product.Code}}/{{Product.Code}}.jpg"  alt="{{Product.Description}}" onerror="this.src='{{ Website.StaticContentUrl }}/assets/otfound-oven.jpg';" />
        {% if Product.WebsiteOverlayImages_Code %}
        <img class="overlay" src="{{ Website.StaticContentUrl }}/pg/{{ Product.WebsiteOverlayImages_Code }}.png"/>
        {% endif %}
    </a>
    <a href="{{Product.NavigateUrl}}" class="product-description" data-productId="{{Product.Id}}" data-productCode="{{Product.Code}}">
  	    <h2 itemprop="name">{{Product.Description}}</h2>
        {{Product.Answer_PSD | Prepend: '<span itemprop="description show-for-medium">' | Append: '</span>'}} 
    </a>
    {{Product.Answer_EXTRA | Prepend: '<span class="product-description" itemprop="Description">' | Append: '</span>' }}
    <div itemprop="offers" class="offers" itemscope itemtype="http://schema.org/Offer">
        <span itemprop="pricecurrency" style="display:none;">GBP</span>
  		<span itemprop="price">{{ Product.Price_VatInclusivePrice | Round:2 | FormatCurrency  : ActiveCurrency }}</span><span class="vat"> (Inc. Vat)</span>
        <span itemprop="price">{{ Product.Price_VatExclusivePrice | Round:2 | FormatCurrency  : ActiveCurrency }}</span><span class="vat"> (Ex. Vat)</span>
    </div>
</article>
{% endfor %}
```
{% endraw %}

---

<a name="advanced"></a>
### Advanced
List / Grid view options.
Create a new snipped named "PARTIAL.PRODUCT-LISTING"

<div class="example-title">PARTIAL.PRODUCT-LISTING</div>
{% raw %}
```liquid
{% assign maxPages = 5 %}
{% assign previousPages = 2 %}
{% assign nextPages = 2 %}
{% if Navigation.Paging.PageNumber > (previousPages + nextPages - 1) %}
    {% if Navigation.Paging.PageNumber + nextPages > Navigation.Paging.NumberOfPages %}
        {% assign lastPage = Navigation.Paging.PageNumber | Plus: nextPages %}
        {% if lastPage > Navigation.Paging.NumberOfPages %}
            {% assign lastPage = Navigation.Paging.NumberOfPages %}
        {% endif %}
        {% assign firstPage = lastPage | Minus: maxPages | Plus: 1 %}
        {% if firstPage < 1 %}
            {% assign firstPage = 1 %}
        {% endif %}
    {% endif %}
{% else %}
    {% assign firstPage = 1 %}
    {% assign lastPage = maxPages %}
    {% if lastPage > Navigation.Paging.NumberOfPages %}
        {% assign lastPage = Navigation.Paging.NumberOfPages %}
    {% endif %}
{% endif %}
{% if UserSetting["list-view"].Value == "grid" %}
    {% include PARTIAL.PRODUCT-LISTING.GRID %}
{% else %}
    {% include PARTIAL.PRODUCT-LISTING.LIST %}
{% endif %}
```
{% endraw %}

<div class="example-title">PARTIAL.PRODUCT-LISTING.LIST / PARTIAL.PRODUCT-LISTING.GRID</div>
{% raw %}
```liquid
{% include "PARTIAL.PRODUCT-LISTING.PAGING" %}
{% for Product in HierarchyNode.Products %}
<article itemscope itemtype="http://schema.org/Product">
    <div class="product-img">
    {% if Product.WebsiteOverlayImages_Code %}
        <img class="overlay" src="{{ Website.StaticContentUrl }}/pg/{{ Product.WebsiteOverlayImages_Code }}.png" onerror='this.style.display = "none"' alt=""  />
    {% endif %}
	    <a href="{{Product.NavigateUrl}}" class="product-image" data-productId="{{Product.Id}}" data-productCode="{{Product.Code}}">
	        <object data="{{ Website.StaticContentUrl }}/p/s/{{Product.Code}}/{{Product.Code}}.jpg" type="image/png">
	           <img id="{{ Product.Code }}" src="{{ Website.StaticContentUrl }}/p/s/not_found.jpg"  alt="{{Product.Description}}" />
	        </object>
	    </a>
    </div>
    <a href="{{Product.NavigateUrl}}" class="product-description" data-productId="{{Product.Id}}" data-productCode="{{Product.Code}}">
        <h2 itemprop="name">{{Product.Description}}</h2>
    </a>
    <div itemprop="offers" itemscope itemtype="http://schema.org/Offer">
        <span itemprop="pricecurrency" style="display:none;">GBP</span>
        <span class="price">
            <span itemprop="price">{{ Product.ProductPrice.VatInclusivePrice | Round:2 | FormatCurrency  : ActiveCurrency }}</span>
            {% if Product.GBPWasPrice_VatInclusivePrice > 0 %}
            <span class="rrp">WAS {{ Product.ProductPrices["ProductWasPrice"].VatInclusivePrice | Round: 2 | FormatCurrency  : ActiveCurrency }}</span>
            {% endif %}
        </span>
    </div>
</article>
{% endfor %} 
{% include "PARTIAL.PRODUCT-LISTING.PAGING" %}
```
{% endraw %}