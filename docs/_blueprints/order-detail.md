---
layout: collection
title: Order Detail
name: order-detail
description: Blueprint for the order detail page.
---

**Order Detail**

<div class="example-title">Input</div>
{% raw %}
```liquid
<section class="order-detail">
    {% if TransactionHeader %}
    <h2>Order Detail</h2>
    {% if TransactionLines %}
    <div class="transaction-details">
        <h3>Transaction Details</h3>
        <span>Order Ref: {{ TransactionHeader.Reference }}</span>
        <span>Order Date: {{ TransactionHeader.OrderDate | DateOnly }}</span>
    </div>
    <ul class="order-detail-basket">
        <li class="headings">
            <span class="basket-description">Product Description</span>
            <span class="basket-item-price">Price</span>
         	<span class="basket-qty">Qty</span>
            <span class="basket-total">Total</span>                
        </li>
        {% for transactionLine in TransactionLines %}
        <li>
            <span class="basket-description">{{transactionLine.Product.Description}}</span>
            <span class="basket-item-price">{{transactionLine.Price | Round : 2 | FormatCurrency  : ActiveCurrency}}</span>
            <span class="basket-qty">{{transactionLine.Quantity | Round : 0 }}</span>
            <span class="basket-total">{{transactionLine.LineValueIncludingVat | Round : 2 | FormatCurrency  : ActiveCurrency}}</span>
        </li>
        {% endfor %}
    </ul>
  	<div class="order-totals">
        <ul>
            <li>ITEMS:{{ TransactionHeader.TotalQuantity | Round : 0  }}</li>
            <li>TOTAL:{{ TransactionHeader.GoodsGrossRounded | Round: 2 | FormatCurrency  : ActiveCurrency}} (inc.VAT)</li>
            <li>DELIVERY:{{ TransactionHeader.DispatchGrossRounded | Round : 2 | FormatCurrency  : ActiveCurrency}} (inc.VAT)</li>
            <li>GRAND TOTAL:{{ TransactionHeader.GoodsGrossRounded  | Round: 2 | Plus: TransactionHeader.DispatchGrossRounded | Round : 2 | FormatCurrency  : ActiveCurrency}} (inc.VAT)</li>
        </ul>
    </div>
    <a href="{{ Endpoints.OrderEnquiryPage.Url }}">Back To Enquiry Page</a> 
    {% endif %}
    <div class="medium-4 columns">
      {% if Address %}
        <div class="transaction-details">
            <h3>Billing Address</h3>
            <span>{{ Address.AddressLine1 }}</span>
            <span>{{ Address.AddressLine2 }}</span>
            <span>{{ Address.AddressLine3 }}</span>
            <span>{{ Address.AddressLine4 }}</span>
            <span>{{ Address.AddressLine5 }}</span>
            <span>{{ Address.AddressCountry }}</span>
            <span>{{ Address.Postcode }}</span>
        </div>
        {% endif %}         
        {% if DeliveryAddress %}
        <div class="transaction-details">
            <h3>Delivery Address</h3>
                 <span>{{ DeliveryAddress.AddressLine1 }}</span>
                 <span>{{ DeliveryAddress.AddressLine2 }}</span>
                 <span>{{ DeliveryAddress.AddressLine3 }}</span>
                 <span>{{ DeliveryAddress.AddressLine4 }}</span>
                 <span>{{ DeliveryAddress.AddressLine5 }}</span>
                 <span>{{ DeliveryAddress.AddressCountry }}</span>
                 <span>{{ DeliveryAddress.Postcode }}</span>
             </div>
          {% endif %}                  
          {% if TransactionPayments %}
            <div class="transaction-details">
                <h3>Payment Details</h3>
               {% for transactionPayment in TransactionPayments %}
                <span>Payment Method: {{ transactionPayment.PaymentMethodDescription }}</span>
                <span>{{ transactionPayment.AuthorisationDate   }}</span>
                <span>{{ transactionPayment.MaskedCardNumber }}</span>
                <span>Payment Total: £{{ transactionPayment.Amount | Round: 2 }}</span>
            {%endfor%}
        </div>
       {% endif %}
    </div>
    {% endif %}
</section>
```
{% endraw %}




