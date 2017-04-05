---
layout: collection
title: SortResult
name: sortresult
description: Contains the properties of a column from a data display that is used to sort data, for example on a product listing page.  
 
---

## SortResult

* [ColumName](#columname)
* [ColumnDescription](#columndescription)
* [DataTypeCodeByte](#datatypecodebyte)
* [SortAscending](#sortascending)
* [SortDescending](#sortdescending)

---

<a name="columname"></a>
### ColumName
Determines the name of the column.

{% raw %}
```liquid
{{ SortResult.ColumName }}

```
{% endraw %}

Data Type: string

---

<a name="columndescription"></a>
### ColumnDescription
Determines the sort description of the column.

{% raw %}
```liquid
{{ SortResult.ColumnDescription }}

```
{% endraw %}

Data Type: string

---

<a name="datatypecodebyte"></a>
### DataTypeCodeByte
Determines the type of the data that is to be matched. Defined in the TypeCode enumeration

{% raw %}
```liquid
{{ SortResult.DataTypeCodeByte }}

```
{% endraw %}

Data Type: byte

---

<a name="sortascending"></a>
### SortAscending
True if the results were sorted in ascending order, otherwise false.

{% raw %}
```liquid
{{ SortResult.SortAscending }}

```
{% endraw %}

Data Type: boolean

--- 

<a name="sortdescending"></a>
### SortDescending
True if the results were sorted in descending order, otherwise false.

{% raw %}
```liquid
{{ SortResult.SortDescending }}

```
{% endraw %}

Data Type: boolean

--- 


__link to the NavigationModel__