---
layout: collection
title: Menu Option
name: menuoption
description: The Menu Option Model holds the details of a Menu Option.
 
---

## Menu Option

__This will need more information__


* [Description](#description)
* [UniqueIdentifier](#uniqueidentifier)
* [NavigateUrl](#navigateurl)
* [ShouldProvideCompanyInformationToReport](#shouldprovidecompanyinformationtoreport)
* [ShouldProvideSelectedIdToReport](#shouldprovideselectedidtoreport)

---

<a name="description"></a>
### Description 
The description of the Menu Option

{% raw %}
```liquid
{{ MenuOption.Description }}

```
{% endraw %}

Data Type: string

---

<a name="uniqueidentifier"></a>
### UniqueIdentifier
A unique identifier for the menu option.

{% raw %}
```liquid
{{ MenuOption.UniqueIdentifier }}

```
{% endraw %}

Data Type: guid

---

<a name="navigateurl"></a>
### NavigateUrl
The Url that can be used to get the full details of the Menu Option.

{% raw %}
```liquid
{{ MenuOption.NavigateUrl }}

```
{% endraw %}

Data Type: string

---

<a name="shouldprovidecompanyinformationtoreport"></a>
### ShouldProvideCompanyInformationToReport
Whether company information should be provided to the report.

{% raw %}
```liquid
{{ MenuOption.ShouldProvideCompanyInformationToReport }}

```
{% endraw %}

Data Type: boolean

---		

<a name="shouldprovideselectedidtoreport"></a>
### ShouldProvideSelectedIdToReport
Whether an Id from a selected data grid row should be provided to the report

{% raw %}
```liquid
{{ MenuOption.ShouldProvideSelectedIdToReport }}

```
{% endraw %}

Data Type: boolean

---			
		