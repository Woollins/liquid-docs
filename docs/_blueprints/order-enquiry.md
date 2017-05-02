---
layout: collection
title: Order Enquiry
name: order-enquiry
description: Blueprint for the order enquiry page.
---

**Order Enquiry**

<div class="example-title">Input</div>
{% raw %}
```liquid
<section>
    <article>
        <h1>Orders</h1>
        <div id="order-list">
        {% if TransactionHeaders %}
            <ul class="list">
            {% for transactionHeader in TransactionHeaders %}
                <li class="order-row">
                    <span class="date">{{ transactionHeader.OrderDate | DateOnly }}</span>
                    <span class="ref">{{ transactionHeader.Reference }}</span>
                    <span class="stage"><div>{{ transactionHeader.StageDescription }}</div></span>
                    <span class="qty"><div>{{ transactionHeader.TotalQuantity | Round: 0 }}</div></span>
                    <span class="price"><div><span>{{transactionHeader.GoodsGrossRounded | Round: 2 | FormatCurrency  : ActiveCurrency }}</span></div></span>
                    <span<a href="{{ transactionHeader.OrderDetailNavigateUrl }}">View Order Page</a></span>
                </li>
            {% endfor %}
            </ul>
            {% else %}
            <p>You have no previous orders </p>
        {% endif %}	
        </div>
    </article>
</section>
```
{% endraw %}