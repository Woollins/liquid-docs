---
layout: collection
title: RelatedDataElement
name: relateddataelement
description: __need a description of what RelatedDataElement is__
 
---

## RelatedDataElement

* [Id](#id)
* [Casing](#casing)
* [Code](#code)
* [DecimalPrecision](#decimalprecision)
* [DefaultAnswer](#defaultanswer)
* [Description](#description)
* [DisplayCharacterCountInformation](#displaycharactercountinformation)
* [ElementType](#elementtype)
* [MaximumLengthOrValue](#maximumlengthorvalue)
* [MinimumLengthOrValue](#minimumlengthorvalue)
* [MinimumNumberOfResponses](#minimumnumberofresponses)
* [RegularExpressionForValidation](#regularexpressionforvalidation)
* [Response](#response)
* [Script](#script)

---

<a name="id"></a>
### Id
Determines the Id of the row.

{% raw %}
```liquid
{{ RelatedDataElement.Id }}

```
{% endraw %}

Data Type: int

---

<a name="casing"></a>
### Casing
Defines the casing to use for the element.

{% raw %}
```liquid
{{ RelatedDataElement.Casing }}

```
{% endraw %}

Data Type: Casing Model

__link to the Casing Model__

---

<a name="casing"></a>
### Code
Defines the Code of the element.

{% raw %}
```liquid
{{ RelatedDataElement.Code }}

```
{% endraw %}

Data Type: string

---

<a name="decimalprecision"></a>
### DecimalPrecision
Determines the number of decimal places that decimal data should be captured to.

{% raw %}
```liquid
{{ RelatedDataElement.DecimalPrecision }}

```
{% endraw %}

Data Type: byte

---

<a name="defaultanswer"></a>
### DefaultAnswer
Determines the default answer to use when no answer has been provided.

{% raw %}
```liquid
{{ RelatedDataElement.DefaultAnswer }}

```
{% endraw %}

Data Type: string

---

<a name="description"></a>
### Description
Determines the Description of the element

{% raw %}
```liquid
{{ RelatedDataElement.Description }}

```
{% endraw %}

Data Type: string

---
	
<a name="displaycharactercountinformation"></a>
### DisplayCharacterCountInformation
Determines whether the element should be setup to display a label showing the count of characters entered and the remaining available characters.

{% raw %}
```liquid
{{ RelatedDataElement.DisplayCharacterCountInformation }}

```
{% endraw %}

Data Type: boolean

---

<a name="elementtype"></a>
### ElementType
Defines the type of data that is being captured for this element.

{% raw %}
```liquid
{{ RelatedDataElement.ElementType }}

```
{% endraw %}

Data Type: RelatedDataElementType Model

__RelatedDataElementType Model__

---

<a name="maximumlengthorvalue"></a>
### MaximumLengthOrValue
If greater than zero, this specifies the maximum value that can be entered for numeric fields or the maximum length of data that can be entered for string values.

{% raw %}
```liquid
{{ RelatedDataElement.MaximumLengthOrValue }}

```
{% endraw %}

Data Type: decimal

---

<a name="minimumlengthorvalue"></a>
### MinimumLengthOrValue
__description needed__

{% raw %}
```liquid
{{ RelatedDataElement.MinimumLengthOrValue }}

```
{% endraw %}

Data Type: decimal

---
 
<a name="minimumnumberofresponses"></a>
### MinimumNumberOfResponses
Determines the minimum number of responses. A value of zero indicates that the element can be left empty.

{% raw %}
```liquid
{{ RelatedDataElement.MinimumNumberOfResponses }}

```
{% endraw %}

Data Type: int

---

<a name="permittedresponses"></a>
### PermittedResponses
If the element is configured as a Permitted Response type, the permitted responses will be stored here.

{% raw %}
```liquid
{{ RelatedDataElement.PermittedResponses }}

```
{% endraw %}

Data Type: RelatedDataPermittedResponse Model

__link to the RelatedDataPermittedResponse Model__

---		

<a name="regularexpressionforvalidation"></a>
### RegularExpressionForValidation
__description needed__

{% raw %}
```liquid
{{ RelatedDataElement.RegularExpressionForValidation }}

```
{% endraw %}

Data Type: string

---	

<a name="response"></a>
### Response
If the element has a response, it will be specified here.

{% raw %}
```liquid
{{ RelatedDataElement.Response }}

```
{% endraw %}

Data Type: RelatedDataResponse Model

__link to the RelatedDataResponse Model__

---	

<a name="script"></a>
### Script
__description needed__

{% raw %}
```liquid
{{ RelatedDataElement.Script }}

```
{% endraw %}

Data Type: string

---			