---
layout: collection
title: SearchAutoCompletion
name: searchautocompletion
description: A suggested search AutoCompletion.
 
---

## SearchAutoCompletion

* [HitCount](#hitcount)
* [SearchTerm](#searchterm)

---

<a name="hitcount"></a>
### HitCount
Determines the number of hits that the suggestion would have.

{% raw %}
```liquid
{{ SearchAutoCompletion.HitCount }}

```
{% endraw %}

Data Type: int

---

<a name="searchterm"></a>
### SearchTerm
Determines the suggested search term.

{% raw %}
```liquid
{{ SearchAutoCompletion.SearchTerm }}

```
{% endraw %}

Data Type: string

---