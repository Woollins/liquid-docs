---
layout: collection
title: Sort Option
name: sortoption
description: Represents the data that can be used to sort Product queries.
 
---

## Sort Option

* [ColumnDescription](#columndescription)
* [ColumnName](#columnname)
* [DataTypeCodeByte](#datatypecodebyte)
* [SortAscending](#sortascending)
* [SortDescending](#sortdescending)

---

<a name="columndescription"></a>
### ColumnDescription
Determines the description of the sort column.

{% raw %}
```liquid
{{ Navigation.SortOptions.ColumnDescription }}

```
{% endraw %}

Data Type: string

---

<a name="columnname"></a>
### ColumnName
Determines the name of the sort column

{% raw %}
```liquid
{{ Navigation.SortOptions.ColumnName }}

```
{% endraw %}

Data Type: string

---

<a name="datatypecodebyte"></a>
### DataTypeCodeByte
True if the results were sorted in ascending order, otherwise false.

{% raw %}
```liquid
{{ Navigation.SortOptions.DataTypeCodeByte }}

```
{% endraw %}

Data Type: byte

---

<a name="sortascending"></a>
### SortAscending
True if the results were sorted in ascending order, otherwise false.

{% raw %}
```liquid
{{ Navigation.SortOptions.SortAscending }}

```
{% endraw %}

Data Type: boolean

---

<a name="sortdescending"></a>
### SortDescending
True if the results were sorted in descending order, otherwise false.

{% raw %}
```liquid
{{ Navigation.SortOptions.SortDescending }}

```
{% endraw %}

Data Type: boolean

---		