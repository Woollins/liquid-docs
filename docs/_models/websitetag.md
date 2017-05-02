---
layout: collection
title: WebsiteTag
name: websitetag
description: Provides access to website tags.
 
---

## WebsiteTag

* [DetailedDescription](#detaileddescription)
* [NavigateUrl](#navigateurl)
* [TagName](#tagname)
* [TagNameToUseInUrl](#tagnametouseinurl)

---

<a name="detaileddescription"></a>
### DetailedDescription
Determines the detailed Description of the Tag

{% raw %}
```liquid
{{ WebsiteTag.DetailedDescription }}

```
{% endraw %}

Data Type: string

---

<a name="navigateurl"></a>
### NavigateUrl
Determines the url that can be used to navigate to the page that displays all products for this tag.

{% raw %}
```liquid
{{ WebsiteTag.NavigateUrl }}

```
{% endraw %}

Data Type: string

---

<a name="tagname"></a>
### TagName
Determines the name of the tag

{% raw %}
```liquid
{{ WebsiteTag.TagName }}

```
{% endraw %}

Data Type: string

---

<a name="tagnametouseinurl"></a>
### TagNameToUseInUrl
Determines the TagName field in a URL friendly format. This is field that should be used in URLs.

{% raw %}
```liquid
{{ WebsiteTag.TagNameToUseInUrl }}

```
{% endraw %}

Data Type: string

---