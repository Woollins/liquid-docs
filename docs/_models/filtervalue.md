---
layout: collection
title: FilterValue
name: filtervalue
description: Contains information used to filter Transaction data. Each filter will have a Column, Description and an array of values containing one or more items. 
 
---

## FilterValue

* [Data](#data)
* [TypeCodeByte](#typecodebyte)

---

<a name="data"></a>
### Data
Used to filter Transaction data.

{% raw %}
```liquid
{{ FilterValue.Data }}

```
{% endraw %}

Data Type: string

---

<a name="typecodebyte"></a>
### TypeCodeByte
Defines the type of filter data.

{% raw %}
```liquid
{{ FilterValue.TypeCodeByte }}

```
{% endraw %}

Data Type: byte

---