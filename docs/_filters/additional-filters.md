---
layout: collection
title: Additional Filters
name: additional-filters
description: serve many different purposes including formatting, converting, and applying CSS classes
---

**Additional Filters**
General filters serve many different purposes including formatting, converting, and applying CSS classes.

* [DateOnly](#dateonly) 
* [FormatCurrency](#formatcurrency) 
* [FormatDate](#formatdate) 
* [FormatDateAndTime](#formatdateandtime) 
* [Limit](#limit) 
* [NextPage](#nxtpage) 
* [PageSize](#pagesize) 
* [PreviousPage](#previouspage) 

<a name="dateonly"></a>
### DateOnly 
Filter DataTime object to display date only

{% raw %}
```liquid
{{ transactionHeader.OrderDate | DateOnly }}
```
{% endraw %}
Output: '02/04/2015'

<a name="formatcurrency"></a>
### FormatCurrency 
Formats price to the correct number of decimal places with the appropriate currency symbol
{% raw %}
```liquid
{{ 12.99 | FormatCurrency  : "EUR"}}
```
{% endraw %}
Output: '€12.99'

*__Could do with listing all formats__*

<a name="formatdate"></a>
### FormatDate 
Formats the date to the iso-8601 standard. The time will all be zero
{% raw %}
```liquid
{{response.DateAnswer : FormatDate}}
```
{% endraw %}
*__Could do with more information on this__*

<a name="formatdateandtime"></a>
### FormatDateAndTime 
Formats both the date and time to the iso-8601 standard
{% raw %}
```liquid
{{response.DateAnswer : FormatDateAndTime}}
```
{% endraw %}
*__Could do with more information on this__*

<a name="limit"></a>
### Limit 
Limit the number of loops returned
{% raw %}
```liquid
{% for post in node.Products | limit:5 %}   
```
{% endraw %}
Output: Limits the number of posts returned to 5

<a name="nxtpage"></a>
### NextPage 
Generates a Navigate Url for a Hierarchy Node that goes forward to a new page. The number of pages to go forward can be specified by the parameterer pageArgument. If this is not specified, the link will be for the next page.
{% raw %}
```liquid
{{ Navigation | NextPage }}
```
{% endraw %}
Output: This will take the user to the next page
{% raw %}
```liquid
{{ Navigation | NextPage:2 }}
```
{% endraw %}
Output: This will take the user to page 2
*__Could do with more information on this__*

<a name="pagesize"></a>
### PageSize 
A filter that can generate a navigate url to change the page size. The new page size to used is passed in the newPageSize parameter
{% raw %}
```liquid
{{ Navigation | PageSize:12 }}
```
{% endraw %}
*__Could do with more information on this__*

<a name="previouspage"></a>
### PreviousPage 
Generates a Navigate Url for a Hierarchy Node that goes back to a previous page. The number of pages to go back can be specified by the parameterer pageArgument. If this is not specified, the link will be for the previous page.
{% raw %}
```liquid
{{ Navigation | PreviousPage }}
```
{% endraw %}
Output: This will take the user to the previous page
{% raw %}
```liquid
{{ Navigation | PreviousPage:2 }}
```
{% endraw %}
Output: This will take the user to the previous page
*__Could do with more information on this__*
