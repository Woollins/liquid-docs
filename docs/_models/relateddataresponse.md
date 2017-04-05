---
layout: collection
title: RelatedDataResponse
name: relateddataresponse
description: Represents a response for a RelatedData element
 
---

## RelatedDataResponse

* [Answer](#answer)
* [DateAnswer](#dateanswer)
* [FormattedTextAnswer](#formattedtextanswer)
* [NumericAnswer](#numericanswer)
* [RelatedDataElementId](#relateddataelementid)
* [RelatedDataPermittedResponseId](#relateddatapermittedresponseid)
* [TextAnswer](#textanswer)

---

<a name="answer"></a>
### Answer
Determines the Answer to the Response. TODO: Document what this actually contains

{% raw %}
```liquid
{{ RelatedDataResponse.Answer }}

```
{% endraw %}

Data Type: string

---

<a name="dateanswer"></a>
### DateAnswer
Determines if the Element is configured as a Date or Time type, this will contain the value that was selected.

{% raw %}
```liquid
{{ RelatedDataResponse.DateAnswer }}

```
{% endraw %}

Data Type: DateTime

---

<a name="formattedtextanswer"></a>
### FormattedTextAnswer
Determines if the Element is configured as text and the 'Use Formatted Text', then this will contain the text in a Formatted format.

{% raw %}
```liquid
{{ RelatedDataResponse.FormattedTextAnswer }}

```
{% endraw %}

Data Type: string

---

<a name="numericanswer"></a>
### NumericAnswer
Determines if the Element Type is Numeric, this specifies the answer value stored as numeric.

{% raw %}
```liquid
{{ RelatedDataResponse.NumericAnswer }}

```
{% endraw %}

Data Type: decimal

---

<a name="relateddataelementid"></a>
### RelatedDataElementId
Determines the Id of the RelatedDataElement that the response is for

{% raw %}
```liquid
{{ RelatedDataResponse.RelatedDataElementId }}

```
{% endraw %}

Data Type: int

---

<a name="relateddatapermittedresponseid"></a>
### RelatedDataPermittedResponseId
Determines if the Element is a PermittedResponse type of element, this specifies the Id of the Permitted Response that is being used.

{% raw %}
```liquid
{{ RelatedDataResponse.RelatedDataPermittedResponseId }}

```
{% endraw %}

Data Type: int

---

<a name="textanswer"></a>
### TextAnswer
Determines if the element type is configured as text, this will contain the Text response.

{% raw %}
```liquid
{{ RelatedDataResponse.TextAnswer }}

```
{% endraw %}

Data Type: string

---