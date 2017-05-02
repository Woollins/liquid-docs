---
layout: collection
title: WebsiteForm
name: websiteform
description: Represents a Website Form.
 
---

## WebsiteForm

* [Id](#id)
* [Behaviour](#behaviour)
* [Code](#code)
* [Description](#description)
* [EndpointUrlForCreate](#endpointurlforcreate)
* [EndpointUrlForDetails](#endpointurlfordetails)
* [EndpointUrlForEnquiry](#endpointurlforenquiry)
* [EndpointUrlForProcess](#endpointurlforprocess)
* [LinkToProduct](#linktoproduct)

---

<a name="id"></a>
### Id
Determines the Id of the row.

{% raw %}
```liquid
{{ WebsiteForm.Id }}

```
{% endraw %}

Data Type: int

---

<a name="behaviour"></a>
### Behaviour
Determines the Behaviour of the Website Form

{% raw %}
```liquid
{{ WebsiteForm.Behaviour }}

```
{% endraw %}

Data Type: WebsiteFormBehaviour Model

__link to the WebsiteFormBehaviour Model__

---

<a name="code"></a>
### Code
Determines the website forms code.

{% raw %}
```liquid
{{ WebsiteForm.Code }}

```
{% endraw %}

Data Type: string

---

<a name="description"></a>
### Description
Determines the website forms description

{% raw %}
```liquid
{{ WebsiteForm.Description }}

```
{% endraw %}

Data Type: string

---	

<a name="endpointurlforcreate"></a>
### EndpointUrlForCreate
Determines the URL to post requests to Create transactions for a Website Form.

{% raw %}
```liquid
{{ WebsiteForm.EndpointUrlForCreate }}

```
{% endraw %}

Data Type: string

---	

<a name="endpointurlfordetails"></a>
### EndpointUrlForDetails
Determines the URL to post requests to get Details of the WebsiteForm Form.

{% raw %}
```liquid
{{ WebsiteForm.EndpointUrlForDetails }}

```
{% endraw %}

Data Type: string

---	

<a name="endpointurlforenquiry"></a>
### EndpointUrlForEnquiry
Determines the URL to post requests to get Enquiry of the WebsiteForm Form.

{% raw %}
```liquid
{{ WebsiteForm.EndpointUrlForEnquiry }}

```
{% endraw %}

Data Type: string

---

<a name="endpointurlforprocess"></a>
### EndpointUrlForProcess
Determines the URL to post requests to Process transactions for a Website Form.

{% raw %}
```liquid
{{ WebsiteForm.EndpointUrlForProcess }}

```
{% endraw %}

Data Type: string

---

<a name="linktoproduct"></a>
### LinkToProduct
Determines whether the Website Form is set to link to Product

{% raw %}
```liquid
{{ WebsiteForm.LinkToProduct }}

```
{% endraw %}

Data Type: boolean

---	