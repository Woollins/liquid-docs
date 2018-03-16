The Registration Endpoint is used to Register a user with an Account.

The Endpoint inherits from the [[Base Endpoint]]

The Endpoint provides Read/Write access to the Session state.

==Url==
The Url to access the Endpoint is: <code>~/registration</code>

==Parameters==
{| class="wikitable"
|-
! Name !! Description
|-
| AddressCategories || An array of [[Category Model]]s for the Address Categories to register.
|-
| AddressRelatedData || An array of [[Related Data Response Model]]s for the Address being registered.
|-
| AddressLine1 || The first line of the Address to register.
|-
| AddressLine2 || The second line of the Address to register.
|-
| AddressLine3 || The third line of the Address to register.
|-
| AddressLine4 || The fourth line of the Address to register.
|-
| AddressLine5 || The fifth line of the Address to register.
|-
| CheckoutPageRegistration || Indicates whether the registration is taking place on the Checkout Page.
|-
| ConfirmationEmailAddress || The email address confirmation.
|-
| ConfirmationPassword || The password confirmation.
|-
| ContactCategories || An array of [[Category Model]]s for the Contact being registered.
|-
| CountryCode || The Code of the Country being registered.
|-
| EmailAddress || The new user's email address.
|-
| FirstName || The First Name (forename) for the new Address to register.
|-
| LastName || The Last Name (surname) for the new Address to register.
|-
| MailingPreferenceForEmail || Pass a value of <code>on</code> for this parameter to indicate a Email mailing preference.
|-
| MailingPreferenceForPost || Pass a value of <code>on</code> for this parameter to indicate a Post mailing preference.
|-
| MailingPreferenceForThirdParty || Pass a value of <code>on</code> for this parameter to indicate a Third Party Mailing preference.
|-
| OrganisationName || The Organisation Name for the new Address.
|-
| Password || The new user's password.
|-
| Postcode || The postcode of the Address to register
|-
| Title || The title for the new Address to register
|}

In addition to the above fixed parameters, there are a number of dynamic parameters whose names are determined by the configuration against the website.
===Communication Types===
The [[Communication Type Model]] contains a <code>FieldName</code> property which indicates the name of the parameter that the Communication Type can be passed using.

==Models==
In addition to the Models provided by the [[Base Endpoint]] the following models will also be provided.
{| class="wikitable"
|-
! Name !! Type !! Description
|-
| RegistrationResult || [[Registration Result Model]] || The Registration Result.
|-
| Postal Rule || [[Postal Rule Model]] || The Postal Rule Result.
|}

==Functionality==
If the <code>EmailAddress</code> and <code>Password</code> are valid (and the <code>ConfirmationEmailAddress</code>/<code>ConfirmationPassword</code> match) and there isn't an existing account in the system with the specified email address, then the account will get created.

===JSON Post===

The <code>JSON</code> object returned by the Endpoint contains the following parameters:

{| class="wikitable"
|-
! Name !! Type !! Description
|-
| InvalidCountryCode || bool || True, if the Country Code is invalid.
|-
| EmailAddressesDoNotMatch || bool || True, if the Email Addresses don't match.
|-
| PasswordsDoNotMatch || bool || True, if the Passwords don't match.
|-
| EmailAddressAlreadyRegistered || bool || True, if the Email Address supplied has already been used to create an account.
|-
| RegistrationResult || [[Registration Result Model]] || The Result of the registration.
|}

[[Category:Liquid Endpoints]]



