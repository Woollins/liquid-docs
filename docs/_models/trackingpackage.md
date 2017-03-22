---
layout: collection
title: Tracking Package
name: trackingpackage
description: Contains details of a Package in the Tracking Model.
 
---

## Tracking Package

* [PackageId](#packageid)
* [PackageNumber](#packagenumber)
* [HasBeenDelivered](#hasbeendelivered)
* [DateDelivered](#datedelivered)
* [Events](#events)

---

<a name="packageid"></a>
### PackageId
Determines the Id of the Package.

{% raw %}
```liquid
{{ Tracking.Packages.PackageId }}

```
{% endraw %}

Data Type: int

---

<a name="packagenumber"></a>
### PackageNumber
Determines the Package Number.

{% raw %}
```liquid
{{ Tracking.Packages.PackageNumber }}

```
{% endraw %}

Data Type: string

---

<a name="hasbeendelivered"></a>
### HasBeenDelivered
Determines whether the Package has been delivered.

{% raw %}
```liquid
{{ Tracking.Packages.HasBeenDelivered }}

```
{% endraw %}

Data Type: boolean

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

<a name="events"></a>
### Events
Determines the Tracking Events for this Model.

{% raw %}
```liquid
{{ Tracking.Packages.Events }}

```
{% endraw %}

Data Type: Tracking Package Event Model array

__link to Tracking Package Event Model array__

---