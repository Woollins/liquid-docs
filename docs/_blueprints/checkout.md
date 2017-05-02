---
layout: collection
title: Checkout
name: checkout
description: Blueprint for the checkout page.
---

**Checkout**

<div class="example-title">Basket Section</div>
{% raw %}
```liquid
<div class="checkout-basket">
    <h5>Basket</h5>
    <div id="checkout-user-basket-section">
        {% include PARTIAL.BASKET.CHECKOUT %}
    </div>
</div>
```
{% endraw %}

<div class="example-title">Basket Partial --- "PARTIAL.BASKET.CHECKOUT"</div>
{% raw %}
```liquid
{% if Basket.TransactionLines != null %}   
{% for line in Basket.TransactionLines %}
<div id="{{line.Id}}" class="basket-item">
    <a href="{{line.Product.NavigateUrl}}">
        <object data="{{ Website.StaticContentUrl }}/p/s/{{line.Product.CodeToUseInUrl}}/{{line.Product.CodeToUseInUrl}}.jpg" type="image/png">
            <img id="{{line.Product.CodeToUseInUrl}}" src="{{ Website.StaticContentUrl }}/p/s/not_found.jpg"  alt="{{line.Product.Description}}" />
        </object>
    </a>
    <a href="{{line.Product.NavigateUrl}}">
        <span class="basket-item-description"><span class="basket-item-qty">{{line.Quantity | Round: 0}}x </span>{{ line.Product.Description }} {{ line.Product.Code }}</span>
    </a>
    <span class="basket-price">{{line.LineValueIncludingVat | Round : 2 | FormatCurrency  : ActiveCurrency}}</span>
    <span class="basket-price">{{line.LineValueIncludingVat | Round : 2 | FormatCurrency  : ActiveCurrency}}</span>  
</div>
{% endfor %}
<div id="basket-footer">
    <ul>
        <li>DELIVERY:{{Basket.TransactionHeader.DispatchGrossRounded | Round : 2 | FormatCurrency  : ActiveCurrency}} (inc.VAT)</li>
        {% if Basket.TransactionHeader.DiscountSurchargeGrossRounded > 0 %}
        <li>DISCOUNT:{{ Basket.TransactionHeader.DiscountSurchargeGrossRounded | Round: 2 | FormatCurrency  : ActiveCurrency }}</li>
        <li>SUBTOTAL:£{{Basket.TransactionHeader.GoodsNettRounded | Round : 2}} (ex.VAT)</li>
        <li>TOTAL:£{{Basket.TransactionHeader.GoodsGrossRounded  | Round: 2 | Plus: Basket.TransactionHeader.DispatchGrossRounded | Round : 2 | Minus : Basket.TransactionHeader.DiscountSurchargeGrossRounded | Round: 2 }} (inc.VAT / Delivery)</li>
        {% else %}
        <li>SUBTOTAL:{{Basket.TransactionHeader.GoodsNettRounded | Round : 2 | FormatCurrency  : ActiveCurrency }} (ex.VAT)</li>
        <li>TOTAL:{{Basket.TransactionHeader.GoodsGrossRounded  | Round: 2 | Plus: Basket.TransactionHeader.DispatchGrossRounded | Round : 2 | FormatCurrency  : ActiveCurrency }} (inc.VAT / Delivery)</li>
        {% endif %}
    </ul>
    {% if ApplyVoucherResult %}
        {% if ApplyVoucherResult.Vouchers %}
            Voucher Added
        {% endif %}
    {% endif %}
</div>  
{% endif %}
```
{% endraw %}

<div class="example-title">Address Section </div>
{% raw %}
```liquid
{% if SignInDetails.SignedIn %}
{% if Address %}
<article class="checkout-address-box primary-address completed">
    <h5>Your Account Details</h5>
	<div class="billing-address-item">
	    <h6>Billing Address</h6><br />
	    <strong>{{Address.OrganisationName}}</strong><br /> 
	    {{Address.AddressLine1}} {{Address.AddressLine2}} {{Address.AddressLine3}} {{Address.AddressLine4}} {{Address.AddressLine5}} {{Address.AddressCountry.Description}} {{Address.Postcode}}
	</div>                        
</article>
<article id="delivery-container" class="checkout-address-box">
    <h5>Your delivery address</h5>
    <div class="checkout-address-item">
    	{% if Address.Id == Basket.TransactionHeader.AddressIdForTransactionDelivery %}
        <input type="radio" id="del-{{Address.Id}}" name="delivery-address" value="{{Address.Id}}" checked>
        {% else %}
        <input type="radio" id="del-{{Address.Id}}" name="delivery-address" value="{{Address.Id}}">
        {% endif %}
        <label class="address-text" for="del-{{Address.Id}}">
            <strong>Use Billing Address (Select if you wish to use Click & Collect)</strong> 
        </label>
    </div>
    {% if Address.DeliveryAddresses != null %}
        {% for address in Address.DeliveryAddresses %}
        <div class="checkout-address-item">
            {% if address.Id == Basket.TransactionHeader.AddressIdForTransactionDelivery %}
                <input type="radio" name="delivery-address" id="del-{{address.Id}}" value="{{address.Id}}" checked>
            {% else %}
                <input type="radio" name="delivery-address" id="del-{{address.Id}}" value="{{address.Id}}">
            {% endif %}
            <label for="del-{{address.Id}}" class="address-text">
                {{address.OrganisationName | Prepend: '<strong>' | Append: '</strong> - '}}{{address.AddressLine1}} {{address.AddressLine2}} {{address.AddressLine3}} {{address.AddressLine4}} {{address.AddressLine5}} {{address.AddressCountry.Description}} {{address.Postcode}}
            </label>
        </div>
        {% include BASKETDELIVERYADDRESS.ADD %}
        {% endfor %}
    {% endif %}
</article>
{% endif %}
```
{% endraw %}

<div class="example-title">Edit Billing Address</div>
{% raw %}
```liquid
<form class="edit-primary-address-form" action="{{Endpoints.EditPrimaryAddress.Url}}" method="post">              
    {% if Website.Countries %}
    <label>
        {{ country.Code }}
        <select id="postcode-lookup-country" name="CountryCode" data-country> 
            {% for country in Website.Countries %}                            
            <option value="{{country.Code}}" {% if Address.AddressCountry.Code == country.Code %} selected {% endif %} data-postal-rule-id="{{country.CategoryIdForPostalRule}}">{{country.Description}}</option>
            {% endfor %}
        </select>
    </label>
    {% endif %}
    {% if Address.IsIndividual %}
    <label>
        <select id="title-select" name="{{ Endpoints.EditPrimaryAddress.TitleParameterName }}">
	        <option value="Mr">Mr</option>
            <option value="Ms">Ms</option>
            <option value="Mrs">Mrs</option>
            <option value="Miss">Miss</option>
        </select>
    </label>
    <label><input type="text" name="{{ Endpoints.EditPrimaryAddress.FirstNameParameterName }}" value="{{ Address.AddressContacts[0].FirstName }}" placeholder="First Name" /></label>
    <label><input type="text" name="{{ Endpoints.EditPrimaryAddress.LastNameParameterName }}" value="{{ Address.AddressContacts[0].LastName }}" placeholder="Last Name"  /></label>
    {% else %}
    <label><input type="text" name="{{ Endpoints.EditPrimaryAddress.OrganisationNameParameterName }}" value="{{ Address.OrganisationName }}" placeholder="Organisation"  /></label>
    {% endif %}
    <label><input type="text" data-addressline1 name="{{ Endpoints.EditPrimaryAddress.AddressLine1ParameterName }}" value="{{ Address.AddressLine1 }}" placeholder="Address Line 1"  /></label>
    <label><input type="text" data-addressline2 name="{{ Endpoints.EditPrimaryAddress.AddressLine2ParameterName }}" value="{{ Address.AddressLine2 }}" placeholder="Address Line 2"  /></label>
    <label><input type="text" data-addressline3 name="{{ Endpoints.EditPrimaryAddress.AddressLine3ParameterName }}" value="{{ Address.AddressLine3 }}" placeholder="Address Line 3" /></label>
    <label><input type="text" data-addressline4 name="{{ Endpoints.EditPrimaryAddress.AddressLine4ParameterName }}" value="{{ Address.AddressLine4 }}" placeholder="City / Town" /></label>
    <label><input type="text" data-addressline5 name="{{ Endpoints.EditPrimaryAddress.AddressLine5ParameterName }}" value="{{ Address.AddressLine5 }}" placeholder="State / County" /></label>
    <label><input  type="text" name="{{ Endpoints.EditPrimaryAddress.PostcodeParameterName }}" value="{{ Address.Postcode }}" placeholder="Postal Code" required /></label>
    <button type="submit">Save</button>
</form>
```
{% endraw %}

<div class="example-title">Add Delivery Address - "BASKETDELIVERYADDRESS.ADD"</div>
{% raw %}
```liquid
<form id="del-form" class="add-delivery-address-form" action="{{Endpoints.CreateDeliveryAddress.Url}}" method="post" data-abide="ajax" novalidate>
 	{% if Address.IsIndividual %}
    <label><input type="text" name="{{Endpoints.CreateDeliveryAddress.FirstNameParameterName}}" placeholder="First Name" required /></label>
    <label><input type="text" name="{{Endpoints.CreateDeliveryAddress.LastNameParameterName}}" placeholder="Last Name" required /></label>
    {% else %}
    <label><input type="text" name="OrganisationName" placeholder="Organisation Name" /></label>
    {% endif %}
 	{% if Website.Countries %}
    <select name="{{ Endpoints.EditPrimaryAddress.CountryCodeParameterName }}">
    	{% for country in Website.Countries %}
        <option value="{{ country.Code }}" {% if Address.AddressCountry.Code == country.Code %} selected {% endif %}>{{ country.Description }}</option>
      	{% endfor %}
    </select>
  	{% endif %}
  	<label><input type="text" name="{{ Endpoints.CreateDeliveryAddress.AddressLine1ParameterName }}" placeholder="Address Line 1"  /></label>
 	<label><input type="text" name="{{ Endpoints.CreateDeliveryAddress.AddressLine2ParameterName }}" placeholder="Address Line 2"  /></label>
    <label><input type="text" name="{{ Endpoints.CreateDeliveryAddress.AddressLine3ParameterName }}" placeholder="Address Line 3"  /></label>
	<label><input type="text" name="{{ Endpoints.CreateDeliveryAddress.AddressLine4ParameterName }}" placeholder="City / Town"  /></label>
    <label><input type="text" name="{{ Endpoints.CreateDeliveryAddress.AddressLine5ParameterName }}" placeholder="State / County"  /></label>
    <label><input type="text" name="{{ Endpoints.CreateDeliveryAddress.PostcodeParameterName}}" placeholder="Postal Code"  /></label>
    <button type="submit">Create</button>
</form>
```
{% endraw %}

<div class="example-title">Login Section</div>
{% raw %}
```liquid
{% else %}
<article class="checkout-login">
    <h5>Sign In</h5>
    <form class="user-sign-in-form" action="{{Endpoints.SignIn.Url}}" method="post" data-abide novalidate data-reload-page-on-success="true">
        <label>
            <input type="email" name="EmailAddress" placeholder="Email" required pattern="email" />
        </label>
        <label>
            <input type="password" name="Password" placeholder="Password" required  />
            <span id="signInError"  class="form-error" style="display:none">Invalid Email Address or Password</span>
        </label>
        <button class="button" type="submit" value="Create">Submit</button>
        <div style="display:block; margin-top:10px;"><a href="{{ Endpoints.ResetPasswordInitiation.Url }}">Forgot your password?</a></div>
    </form>
</article>
<article class="checkout-reg">
    <h5>Your Account Details</h5>
    {% include PARTIAL.REGISTRATION %}
</article>
{% endif %}
```
{% endraw %}

<div class="example-title">Delivery Details</div>
{% raw %}
```liquid
<h5>Your delivery details</h5>
<div id="dispatch-service-level-section">
    {% include PARTIAL.DISPATCHSERVICELEVEL %}
</div>
```
{% endraw %}

<div class="example-title">Delivery Options -- "PARTIAL.DISPATCHSERVICELEVEL" </div>
{% raw %}
```liquid
{% if DispatchServiceLevelResult && DispatchServiceLevelResult.DispatchServiceLevels %}
    {% for dispatchServiceLevel in DispatchServiceLevelResult.DispatchServiceLevels %}
        <div class="checkout-dispatch-service-item">
            <input type="radio" name="dispatch-service-level" id="dsl-{{dispatchServiceLevel.CategoryIdForDispatchServiceLevel}}" value="{{dispatchServiceLevel.CategoryIdForDispatchServiceLevel}}" {% if dispatchServiceLevel.CategoryIdForDispatchServiceLevel == DispatchServiceLevelResult.SelectedDispatchServiceLevel.CategoryIdForDispatchServiceLevel %} checked {% endif %} {% if dispatchServiceLevel.CarrierServiceLevelIsCollection %}data-collection-carrier{% endif %}> 
            <label for="dsl-{{dispatchServiceLevel.CategoryIdForDispatchServiceLevel}}">{{dispatchServiceLevel.DispatchServiceLevelDescription}} {{dispatchServiceLevel.Charge | FormatCurrency}}</label>
        </div>
    {% endfor %} 
    {% if DispatchServiceLevelResult.SelectedDispatchServiceLevel.CarrierServiceLevelIsCollection %}
    	<div class="error-collection-address-required" style="display:none">
    		Please select a collection address
    	</div>
    	{% if Addresses.size > 0 %} 
    		<select class="collection-addresses"> 
    			{% for address in Addresses %} 
    			    {% assign addressInformation = address.AddressLine1 %}
    			    {% if address.AddressLine2 %} {% assign addressInformation = addressInformation | Append: ', ' | Append: address.AddressLine2 %} {% endif %}
    			    {% if address.AddressLine3 %} {% assign addressInformation = addressInformation | Append: ', ' | Append: address.AddressLine3 %} {% endif %}
    			    {% if address.AddressLine4 %} {% assign addressInformation = addressInformation | Append: ', ' | Append: address.AddressLine4 %} {% endif %}
    			    {% if address.AddressLine5 %} {% assign addressInformation = addressInformation | Append: ', ' | Append: address.AddressLine5 %} {% endif %}
    			    {% if address.Postcode %} {% assign addressInformation = addressInformation | Append: ', ' | Append: address.Postcode %} {% endif %}
    				<option value="{{address.Id}}" {% if DispatchServiceLevelResult.SelectedCollectionAddressId == address.Id %}selected="selected"{% endif %}>{{addressInformation}}</option> 
    			{% endfor %} 
    		</select> 
    	{% endif %} 
    {% endif %}
{% endif %}
```
{% endraw %}

<div class="example-title">Payment Section</div>
{% raw %}
```liquid
<div class="checkout-payment-box">
	<h5>Secure payment</h5>
    <div class="payment-container">
    	{% if HoldReasonForPaymentFailure %}
        <span class="warning">Payment Failed</span>
        <div class="error">
            {{HoldReasonForPaymentFailure.Details}}
        </div>
        {% endif %}
        <div id="payment-portal-failure-message" class="error" style="display:none">
            It was not possible to begin payment for this order. Check your shipping address for any missing information.
        </div>
        <div id="payment-method-section">
            {% include PARTIAL.PAYMENTMETHODS %}
        </div>
        <div id="payment-portal-section">
            {% include PARTIAL.PAYMENTPORTAL %}
        </div>
        <div class="complete-order-button-section" style="display: none;">
            <span style="margin-top: 10px;" class="complete-order-button-selector button large">Complete Order</span>
        </div>
    </div>
</div>
```
{% endraw %}


<div class="example-title">Payment Methods -- "PARTIAL.PAYMENTMETHODS" </div>
{% raw %}
```liquid
{% if PaymentMethods %}
    {% for paymentMethod in PaymentMethods %}
        {% if paymentMethod.IsPay4LaterFinance == false %} <div class="checkout-paymentmethod-item"> {% endif %}
            {%if paymentMethod.IsPayPalExpress %}
                <button class="button" id="paypal-{{paymentMethod.CategoryIdForPaymentMethod}}" name="paypal" data-custom-payment-category-id="{{paymentMethod.CategoryIdForPaymentMethod}}">Pay By {{paymentMethod.Description}}</button>
            {% elsif paymentMethod.IsPay4LaterFinance && paymentMethod.PaymentMethodFinanceOptions %}
                {% for financeOption in paymentMethod.PaymentMethodFinanceOptions %}
                    <div class="checkout-paymentmethod-item"> 
                        <input type="radio" id="{{financeOption.FinanceSystemProductCode}}" name="payment-method" value="{{paymentMethod.CategoryIdForPaymentMethod}}" data-payment-method-finance-option-id="{{financeOption.Id}}">
                        <label for="{{financeOption.FinanceSystemProductCode}}">{{financeOption.Description}}</label>
                    </div>
                {% endfor %}
            {%else%}
                <input type="radio" id="{{paymentMethod.CategoryIdForPaymentMethod}}" name="payment-method" value="{{paymentMethod.CategoryIdForPaymentMethod}}">
                <label for="{{paymentMethod.CategoryIdForPaymentMethod}}">{{paymentMethod.Description}}</label>
            {%endif%}
        {% if paymentMethod.IsPay4LaterFinance == false %} </div> {% endif %}
    {% endfor %} 
{% endif %}
```
{% endraw %}

<div class="example-title">Payment Portal -- "PARTIAL.PAYMENTPORTAL" </div>
{% raw %}
```liquid
{% if PaymentPortal %}
    <iframe src="{{ PaymentPortal.NavigateUrl }}" width="100%" height="300px"></iframe>
{% endif %}
```
{% endraw %}