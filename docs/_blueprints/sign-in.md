---
layout: collection
title: Sign in page
name: sign-in
description: Blueprint for the sign in page.
---

**Sign in page**  
Setup a new physical page and add the following code. 

<div class="example-title">Input</div>
{% raw %}
```liquid
<section>
    <article class="login">  
        <form class="user-sign-in-form" action="{{Endpoints.SignIn.Url}}" method="post">
            <label>
                <input type="email" name="EmailAddress" placeholder="Email" required pattern="email" />
            </label>
            <label>
                <input type="password" name="Password" placeholder="Password" required  />
                <span id="signInError"  class="form-error" style="display:none">Invalid Email Address or Password</span>
            </label>
            <button class="button" type="submit" value="Create">Submit</button>
        </form>
        <div><a href="{{ Endpoints.ResetPasswordInitiation.Url }}">Forgot your password?</a></div>
    </article>
    <article class="register">
        <a href="{{ Endpoints.RegistrationPage.Url }}" class="button">Register</a>
    </article>
</section>
```
{% endraw %}
<div class="example-title">Scripts</div>
{% raw %}
```html
<script>
EAWeb.User.OnInvalidEmailAddressOrPassword = function() {
       $("#signInError").css("display", "block"); 
       $( ".button" ).prop( "disabled", false );
}
</script>
```
{% endraw %}


