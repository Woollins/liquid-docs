---
layout: collection
title: CommunicationType
name: communicationtype
description: Describes a communication field to be used on a registration form.
 
---

## CommunicationType

* [CategoryIdForCommunicationType](#categoryidforcommunicationtype)
* [Code](#Code)
* [Description](#description)
* [FieldName](#fieldname)
* [IsEmailAddress](#isemailaddress)
* [IsRequired](#isrequired)
* [IsTelephoneNumber](#istelephonenumber)
* [StoredDetails](#storeddetails)


---

<a name="categoryidforcommunicationtype"></a>
### CategoryIdForCommunicationType
Determines the Category Id for Communication Type.

{% raw %}
```liquid
{{ CommunicationType.CategoryIdForCommunicationType }}

```
{% endraw %}

Data Type: int

---

<a name="code"></a>
### Code
Determines the Code as defined by the communication type.

{% raw %}
```liquid
{{ CommunicationType.Code }}

```
{% endraw %}

Data Type: string

---

<a name="description"></a>
### Description
Determines the Description of the communication field.

{% raw %}
```liquid
{{ CommunicationType.Description }}

```
{% endraw %}

Data Type: string

---

<a name="fieldname"></a>
### FieldName
Specifies the name to use for the input field that is submitted when the form is posted back to the server. 

{% raw %}
```liquid
<input type="text" name="{{ CommunicationType.FieldName }}" />

```
{% endraw %}

Data Type: string

---

<a name="isemailaddress"></a>
### IsEmailAddress
True if the communication field is an email address.

{% raw %}
```liquid
{{ CommunicationType.IsEmailAddress }}

```
{% endraw %}

Data Type: boolean

---


<a name="isrequired"></a>
### IsRequired
True if the communication field is required.

{% raw %}
```liquid
{{ CommunicationType.IsRequired }}

```
{% endraw %}

Data Type: boolean

---

<a name="istelephonenumber"></a>
### IsTelephoneNumber
True if the communication field is a telephone number.

{% raw %}
```liquid
{{ CommunicationType.IsTelephoneNumber }}

```
{% endraw %}

Data Type: boolean

---

<a name="storeddetails"></a>
### StoredDetails
Details for the current communication type.

{% raw %}
```liquid
{{ CommunicationType.StoredDetails }}

```
{% endraw %}

Data Type: string

---