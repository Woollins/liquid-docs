---
layout: collection
title: Recently Viewed Products
name: recently-viewed-products
description: Blueprint for displaying Recently Viewed Products.
---

### Recently Viewed Products

**Recently Viewed Products Scripts**

Add the following script to the script partial. 

<div class="example-title">Script</div>
{% raw %}
```liquid
{% if RecentlyViewedProducts.Ids and RecentlyViewedProducts.Ids.size > 0 %} 
  var arrayOfIds = [];
  {% for id in RecentlyViewedProducts.Ids %}
    arrayOfIds.push({{ id }});
  {% endfor %}
  EAWeb.ProductListing.GetRecentlyViewedProducts(arrayOfIds);
{% endif %}
```
{% endraw %}

**PARTIAL.RECENTLYVIEWEDPRODUCTS**

Create a partial named "PARTIAL.RECENTLYVIEWEDPRODUCTS". Enter the code below.

<div class="example-title">Input</div>
{% raw %}
```liquid
{% if Products %}
    <section class="recent-products">
        <button class="clear" onclick="EAWeb.Product.RemoveRecentlyViewedProducts()">Clear Products</button>
        {% for Product in Products %}
            {% if Product.FormOfProduct.IsVariantBase %}
                <article>
                    <div class="image">
                        <a href="{{Product.NavigateUrl}}" class="product-image" data-productId="{{Product.Id}}" data-productCode="{{Product.Code}}">
                            <object data="{{ Website.StaticContentUrl }}/p/s/{{Product.Code}}/{{Product.Code}}.jpg" type="image/png">
                                <img id="{{ Product.Code }}" src="{{ Website.StaticContentUrl }}/p/s/not_found.jpg"  alt="{{Product.Description}}" />
                            </object>
                        </a>
                        {% if Product.WebsiteOverlayImages_Code %}
                            <img class="overlay" src="{{ Website.StaticContentUrl }}/pg/{{ Product.WebsiteOverlayImages_Code }}.png"  onerror='this.style.display = "none"' />
                        {% endif %}
                    </div>
                    <a href="{{Product.NavigateUrl}}" class="product-description" data-productId="{{Product.Id}}" data-productCode="{{Product.Code}}">
                        {{Product.Description}}
                    </a>
                    <span class="price"><span itemprop="price">{{ Product.ProductPrice.VatInclusivePrice | Round:2 | FormatCurrency  : ActiveCurrency }}</span></span>
                </article>
            {% else %}
                <article>
                    <div class="image">
                        <a href="{{Product.NavigateUrl}}" class="product-image" data-productId="{{Product.Id}}" data-productCode="{{Product.Code}}">
                            <object data="{{ Website.StaticContentUrl }}/p/s/{{Product.Code}}/{{Product.Code}}.jpg" type="image/png">
                                <img id="{{ Product.Code }}" src="{{ Website.StaticContentUrl }}/p/s/not_found.jpg"  alt="{{Product.Description}}" />
                            </object>
                        </a>
                        {% if Product.WebsiteOverlayImages_Code %}
                            <img class="overlay" src="{{ Website.StaticContentUrl }}/pg/{{ Product.WebsiteOverlayImages_Code }}.png" onerror='this.style.display = "none"' />
                        {% endif %}
                    </div>
                    <a href="{{Product.NavigateUrl}}" class="product-description" data-productId="{{Product.Id}}" data-productCode="{{Product.Code}}">
                        {{Product.Description}}
                    </a>
                    <span class="price"> <span itemprop="price">{{ Product.ProductPrice.VatInclusivePrice | Round:2 | FormatCurrency  : ActiveCurrency }}</span></span>
                </article>
            {% endif %}
        {% endfor %}
    </section>
{% endif %}
```
{% endraw %}

<div class="example-title">Include Recently Viewed Products on page</div>
{% raw %}
```html
<div id="recently-viewed-products-section" {%if RecentlyViewedProducts.Ids %}data-recently-viewed-product-ids="{%for id in RecentlyViewedProducts.Ids%}{%if forloop.last%}{{id}}{%else%}{{id}},{%endif%}{%endfor%}"{%endif%}></div>      
```
{% endraw %}

<div class="example-title">Output</div>
{% raw %}
```html
<section class="recent-products">
        <button class="clear" onclick="EAWeb.Product.RemoveRecentlyViewedProducts()">Clear Products</button>     
        <article>
            <div class="image">
                <a href="/pd/leica-8x20-br-ultravid-black-binoculars-40252_40252" class="product-image" data-productid="7267" data-productcode="40252">
                    <object data="/PRODUCT-CODE.jpg" type="image/png">
                        <img id="40252" src="/not_found.jpg" alt="Product Image">
                    </object>
                </a>
            </div>
            <a href="/pd/leica-8x20-br-ultravid-black-binoculars-40252_40252" class="product-description" data-productid="7267" data-productcode="40252">
                Leica 8x20 BR Ultravid Black Binoculars 40252
            </a>
            <span class="price"> <span itemprop="price">£572,51</span></span>
        </article>
</section>          
```
{% endraw %}


