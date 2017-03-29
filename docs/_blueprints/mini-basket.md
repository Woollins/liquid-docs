---
layout: collection
title: Mini Basket
name: mini-basket
description: Blueprint for displaying the mini basket on your website.
---

### Mini Basket

Create a basket snippet and name it "PARTIAL.BASKET".

<div class="example-title">PARTIAL.BASKET</div>
{% raw %}
```liquid
{% if Basket.TransactionLines != null and Basket.TransactionLines.size > 0 %}
<a href="/Basket" class="basketLink">
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
<div class="basket-header basket-empty">
    BASKET 0
</div>
{% endif %}
```
{% endraw %}

Create a second snippet and name it "MINI.BASKET.REMOVE".

<div class="example-title">MINI.BASKET.REMOVE</div>
{% raw %}
```html
<form class="basket-item-remove-form" action="{{Endpoints.RemoveFromBasket.Url}}" method="post">
    <input name="TransactionLineId" type="hidden" value="{{line.Id}}">
    <input type="submit" class="remove-button" value="">
</form>
```
{% endraw %}

Next you can add the mini basket to your page. 

<div class="example-title">Input</div>
{% raw %}
```html
<div id="mini-basket-section"></div>
```
{% endraw %}