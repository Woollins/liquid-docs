---
layout: collection
title: SearchHit
name: searchhit
description: __need more details__
 
---

## SearchHit

* [Id](#id)
* [Scrore](#scrore)

---

<a name="id"></a>
### Id
Determines the Id of the associated data row.

{% raw %}
```liquid
{{ SearchHit.Id }}

```
{% endraw %}

Data Type: int

---

<a name="scrore"></a>
### Scrore
Determines the score for the search hit.

{% raw %}
```liquid
{{ SearchHit.Scrore }}

```
{% endraw %}

Data Type: decimal

---