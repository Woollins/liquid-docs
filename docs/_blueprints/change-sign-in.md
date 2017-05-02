---
layout: collection
title: Change Sign In
name: change-sign-in
description: Blueprint for the change sign in page.
---

**Change sign in details**  
Create a new physical page and add the following code.
<div class="example-title">Input</div>
{% raw %}
```liquid
<section>
    <h1>Change My Sign In Details</h1>
    <div class="updateForm">
	    <form id="update-sign-in-details-section" action="{{Endpoints.UpdateSignInDetails.Url}}" method="post">
	        <div id="updateSignInDetailsSection">
	            <label>
	                <input type="email" id="checkEmail" name="EmailAddress" placeholder="Email" pattern="email" />
	            </label>
	            <label>
	                <input type="email" name="ConfirmationEmailAddress" placeholder="Confirm Email" pattern="email"    />
	            </label>
	            <label>                   
	                <input type="password" name="CurrentPassword"  placeholder="Current Password" />
	            </label>
	            <label>
	                <input type="password" name="NewPassword" id="checkPassword"  placeholder="New Password"  />
	            </label>
	            <label>
	                <input type="password" name="ConfirmNewPassword" placeholder="Confirm Password" />
	            </label>
	            <p id="updateError" class="form-error" style="display:none">Invalid Email Address or Password</p>
	            <input type="submit" class="button hollow" value="Update Details">
	        </div>
	    </form>
    </div>
    <div class="updatemsg" style="display:none; text-align:center;">
        <p>Success your details has been updated.</p>
        <a href="/" class="button hollow">Continue Shopping</a>
    </div>
</section>
```
{% endraw %}

Create a new physical page and add the following code.

<div class="example-title">Scripts</div>
{% raw %}
```html
<!--Script Section-->
<script>
    EAWeb.User.AfterUpdateSignInDetails = function(result) {
        console.log(result);
        if (result.result.InvalidEmailAddressOrPassword == true) {
            $(".updateForm").show();
            $(".updatemsg").hide();
            $("#updateError").show();
        }
        else {
            $( ".button" ).prop( "disabled", false );
            $("#updateError").hide();
            $(".updateForm").hide();
            $(".updatemsg").show();
        }
    }
</script>
```
{% endraw %}


