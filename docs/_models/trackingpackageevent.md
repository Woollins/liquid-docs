---
layout: collection
title: Tracking Package Event
name: trackingpackageevent
description: Contains details of an Event in the Tracking Package Model.
 
---

## Tracking Package Event

* [EventDate](#eventdate)
* [StatusCode](#statuscode)
* [Description](#description)
* [DateDelivered](#datedelivered)
* [Location](#location)

---

<a name="eventdate"></a>
### EventDate
Determines the Date of the event

{% raw %}
```liquid
{{ Tracking.Packages.EventDate }}

```
{% endraw %}

Data Type: DateTime

---

<a name="statuscode"></a>
### StatusCode
Determines the Status Code of the event.

{% raw %}
```liquid
{{ Tracking.Packages.StatusCode }}

```
{% endraw %}

Data Type: string

---

<a name="description"></a>
### Description
Determines the Description of the event

{% raw %}
```liquid
{{ Tracking.Packages.Description }}

```
{% endraw %}

Data Type: string

---

<a name="datedelivered"></a>
### DateDelivered
Determines the DateTime when the package was delivered.

{% raw %}
```liquid
{{ Tracking.Packages.DateDelivered }}

```
{% endraw %}

Data Type: DateTime

---

<a name="location"></a>
### Location
Determines the Location of the Event.

{% raw %}
```liquid
{{ Tracking.Packages.Location }}

```
{% endraw %}

Data Type: string

---