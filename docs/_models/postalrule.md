---
layout: collection
title: PostalRule
name: postalrule
description: The Postal Rule model provides descriptions, minimum characters, sort orders and mnemonics for all of the address fields. It also provides additional properties for the post code such as permitted characters, permitted lengths and a regular expression for validation. The Postal Rule model is used on pages/templates concerned with adding/modifying addresses e.g. the registration and create delivery address templates.
 
---

## PostalRule

* [AddressLine1Label](#addressline1label)
* [AddressLine1MaxChars](#addressline1maxchars)
* [AddressLine1MinChars](#addressline1minchars)
* [AddressLine1SortOrder](#addressline1sortorder)
* [AddressLine2Label](#addressline2label)
* [AddressLine2MaxChars](#addressline2maxchars)
* [AddressLine2MinChars](#addressline2minchars)
* [AddressLine2SortOrder](#addressline2sortorder)
* [AddressLine3Label](#addressline3label)
* [AddressLine3MaxChars](#addressline3maxchars)
* [AddressLine3MinChars](#addressline3minchars)
* [AddressLine3SortOrder](#addressline3sortorder)
* [AddressLine4Label](#addressline4label)
* [AddressLine4MaxChars](#addressline4maxchars)
* [AddressLine4MinChars](#addressline4minchars)
* [AddressLine4SortOrder](#addressline4sortorder)
* [AddressLine5Label](#addressline5label)
* [AddressLine5MaxChars](#addressline5maxchars)
* [AddressLine5MinChars](#addressline5minchars)
* [AddressLine5SortOrder](#addressline5sortorder)
* [CategoryId](#categoryid)
* [NameMaxChars](#namemaxchars)
* [OrganisationNameLabel](#organisationnamelabel)
* [OrganisationNameMaxChars](#organisationnamemaxchars)
* [OrganisationNameMinChars](#organisationnameminchars)
* [OrganisationNameSortOrder](#organisationnamesortorder)
* [PostalLookupEnabled](#postallookupenabled)
* [PostcodeLabel](#postcodelabel)
* [PostcodeMaxChars](#postcodemaxchars)
* [PostcodeMinChars](#postcodeminchars)
* [PostcodePermittedChars](#postcodepermittedchars)
* [PostcodePermittedLengths](#postcodepermittedlengths)
* [PostcodeRegularExpressionForValidation](#postcoderegularexpressionforvalidation)
* [PostcodeSortOrder](#postcodesortorder)

---

<a name="addressline1label"></a>
### AddressLine1Label
Determines the text to use for the Address Line 1 label.

{% raw %}
```liquid
{{ PostalRule.AddressLine1Label }}

```
{% endraw %}

Data Type: string

---

<a name="addressline1maxchars"></a>
### AddressLine1MaxChars
Determines the maximum number of characters to use for the Address Line 1 field.

{% raw %}
```liquid
{{ PostalRule.AddressLine1MaxChars }}

```
{% endraw %}

Data Type: int

---

<a name="addressline1minchars"></a>
### AddressLine1MinChars
Determines the minimum number of characters to use for the Address Line 1 field.

{% raw %}
```liquid
{{ PostalRule.AddressLine1MinChars }}

```
{% endraw %}

Data Type: int

---

<a name="addressline1sortorder"></a>
### AddressLine1SortOrder
Determines the order in which to display the Address Line 1 field.

{% raw %}
```liquid
{{ PostalRule.AddressLine1SortOrder }}

```
{% endraw %}

Data Type: int

---

<a name="addressline2label"></a>
### AddressLine2Label
Determines the text to use for the Address Line 2 label.

{% raw %}
```liquid
{{ PostalRule.AddressLine2Label }}

```
{% endraw %}

Data Type: string

---

<a name="addressline2maxchars"></a>
### AddressLine2MaxChars
Determines the maximum number of characters to use for the Address Line 2 field.

{% raw %}
```liquid
{{ PostalRule.AddressLine2MaxChars }}

```
{% endraw %}

Data Type: int

---

<a name="addressline2minchars"></a>
### AddressLine2MinChars
Determines the minimum number of characters to use for the Address Line 2 field.

{% raw %}
```liquid
{{ PostalRule.AddressLine2MinChars }}

```
{% endraw %}

Data Type: int

---

<a name="addressline2sortorder"></a>
### AddressLine2SortOrder
Determines the order in which to display the Address Line 2 field.

{% raw %}
```liquid
{{ PostalRule.AddressLine2SortOrder }}

```
{% endraw %}

Data Type: int

---

<a name="addressline3label"></a>
### AddressLine3Label
Determines the text to use for the Address Line 3 label.

{% raw %}
```liquid
{{ PostalRule.AddressLine3Label }}

```
{% endraw %}

Data Type: string

---

<a name="addressline3maxchars"></a>
### AddressLine3MaxChars
Determines the maximum number of characters to use for the Address Line 3 field.

{% raw %}
```liquid
{{ PostalRule.AddressLine3MaxChars }}

```
{% endraw %}

Data Type: string

---

<a name="addressline3minchars"></a>
### AddressLine3MinChars
Determines the minimum number of characters to use for the Address Line 3 field.

{% raw %}
```liquid
{{ PostalRule.AddressLine3MinChars }}

```
{% endraw %}

Data Type: int

---

<a name="addressline3sortorder"></a>
### AddressLine3SortOrder
Determines the order in which to display the Address Line 3 field.

{% raw %}
```liquid
{{ PostalRule.AddressLine3SortOrder }}

```
{% endraw %}

Data Type: int

---

<a name="addressline4label"></a>
### AddressLine4Label
Determines the text to use for the Address Line 4 label.

{% raw %}
```liquid
{{ PostalRule.AddressLine4Label }}

```
{% endraw %}

Data Type: int

---

<a name="addressline4maxchars"></a>
### AddressLine4MaxChars
Determines the maximum number of characters to use for the Address Line 4 field.

{% raw %}
```liquid
{{ PostalRule.AddressLine4MaxChars }}

```
{% endraw %}

Data Type: int

---

<a name="addressline4minchars"></a>
### AddressLine4MinChars
Determines the minimum number of characters to use for the Address Line 4 field.

{% raw %}
```liquid
{{ PostalRule.AddressLine4MinChars }}

```
{% endraw %}

Data Type: int

---

<a name="addressline4sortorder"></a>
### AddressLine4SortOrder
Determines the order in which to display the Address Line 4 field.

{% raw %}
```liquid
{{ PostalRule.AddressLine4SortOrder }}

```
{% endraw %}

Data Type: int

---

<a name="addressline5label"></a>
### AddressLine5Label
Determines the text to use for the Address Line 5 label.

{% raw %}
```liquid
{{ PostalRule.AddressLine5Label }}

```
{% endraw %}

Data Type: string

---

<a name="addressline5maxchars"></a>
### AddressLine5MaxChars
Determines the maximum number of characters to use for the Address Line 5 field.

{% raw %}
```liquid
{{ PostalRule.AddressLine5MaxChars }}

```
{% endraw %}

Data Type: int

---

<a name="addressline5minchars"></a>
### AddressLine5MinChars
Determines the minimum number of characters to use for the Address Line 5 field.

{% raw %}
```liquid
{{ PostalRule.AddressLine5MinChars }}

```
{% endraw %}

Data Type: int

---

<a name="addressline5sortorder"></a>
### AddressLine5SortOrder
Determines the order in which to display the Address Line 5 field.

{% raw %}
```liquid
{{ PostalRule.AddressLine5SortOrder }}

```
{% endraw %}

Data Type: int

---

<a name="categoryid"></a>
### CategoryId
Determines the Category Id for the Postal Rule.

{% raw %}
```liquid
{{ PostalRule.CategoryId }}

```
{% endraw %}

Data Type: int

---

<a name="namemaxchars"></a>
### NameMaxChars
Determines the maximum number of characters to use for the Name field.

{% raw %}
```liquid
{{ PostalRule.NameMaxChars }}

```
{% endraw %}

Data Type: int

---

<a name="organisationnamelabel"></a>
### OrganisationNameLabel
Determines the text to use for the Organisation Name label.

{% raw %}
```liquid
{{ PostalRule.OrganisationNameLabel }}

```
{% endraw %}

Data Type: string

---

<a name="organisationnamemaxchars"></a>
### OrganisationNameMaxChars
Determines the maximum number of characters to use for the Organisation Name field.

{% raw %}
```liquid
{{ PostalRule.OrganisationNameMaxChars }}

```
{% endraw %}

Data Type: byte

---

<a name="organisationnameminchars"></a>
### OrganisationNameMinChars
Determines the minimum number of characters to use for the Organisation Name field.

{% raw %}
```liquid
{{ PostalRule.OrganisationNameMaxChars }}

```
{% endraw %}

Data Type: int

---

<a name="organisationnamesortorder"></a>
### OrganisationNameSortOrder
Determines the order in which to display the Organisation Name field.

{% raw %}
```liquid
{{ PostalRule.OrganisationNameSortOrder }}

```
{% endraw %}

Data Type: int

---

<a name="postallookupenabled"></a>
### PostalLookupEnabled
Indicates whether the PostalRule supports Postal Lookup.

{% raw %}
```liquid
{{ PostalRule.PostalLookupEnabled }}

```
{% endraw %}

Data Type: boolean	

---

<a name="postcodelabel"></a>
### PostcodeLabel
Determines the text to use for the Postcode label.

{% raw %}
```liquid
{{ PostalRule.PostcodeLabel }}

```
{% endraw %}

Data Type: string

---

<a name="postcodemaxchars"></a>
### PostcodeMaxChars
Determines the maximum number of characters to use for the Postcode field.

{% raw %}
```liquid
{{ PostalRule.PostcodeMaxChars }}

```
{% endraw %}

Data Type: int

---

<a name="postcodeminchars"></a>
### PostcodeMinChars
Determines the minimum number of characters to use for the Postcode field.

{% raw %}
```liquid
{{ PostalRule.PostcodeMinChars }}

```
{% endraw %}

Data Type: int

---

<a name="postcodepermittedchars"></a>
### PostcodePermittedChars
Determines the permitted Postcode characters.

{% raw %}
```liquid
{{ PostalRule.PostcodePermittedChars }}

```
{% endraw %}

Data Type: byte

---

<a name="postcodepermittedlengths"></a>
### PostcodePermittedLengths
Determines the permitted lengths for the Postcode e.g. 7 PR7 1NS (space is one character)

{% raw %}
```liquid
{{ PostalRule.PostcodePermittedLengths }}

```
{% endraw %}

Data Type: string

---

<a name="postcoderegularexpressionforvalidation"></a>
### PostcodeRegularExpressionForValidation
Determines the regular expression to use for Postcode validation.

{% raw %}
```liquid
{{ PostalRule.PostcodeRegularExpressionForValidation }}

```
{% endraw %}

Data Type: string

---

<a name="postcodesortorder"></a>
### PostcodeSortOrder
Determines the order in which to display the Postcode field.

{% raw %}
```liquid
{{ PostalRule.PostcodeSortOrder }}

```
{% endraw %}

Data Type: int

---