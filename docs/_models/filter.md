---
layout: collection
title: Filter
name: filter
description: Contains information used to filter Transaction data. Each filter will have a Column, Description and an array of values containing one or more items. 
 
---

## Filter

* [Column](#column)
* [Description](#description)
* [Values](#values)

---

<a name="column"></a>
### Column
Determines the column associated with the filter.

{% raw %}
```liquid
{{ Filter.Column }}

```
{% endraw %}

Data Type: string

---

<a name="description"></a>
### Description
Determines the description of the filter. This will default to the value of the column unless updated by a user.

{% raw %}
```liquid
{{ Filter.Description }}

```
{% endraw %}

Data Type: string

---

<a name="values"></a>
### Values
An array of filter values used to filter the Transaction data

{% raw %}
```liquid
{{ Filter.Values }}

```
{% endraw %}

Data Type: Filter Value Model array

__link to the Filter Value Model__

---