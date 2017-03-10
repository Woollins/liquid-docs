---
layout: collection
title: Hierarchy Navigation
name: hierarchy-navigation
description: Blueprint for a typical hierarchy navigation.
---

**Hierarchy navigation** is used to generate links based on a website hierarchy defined within the system.

* [Basic](#basic)
* [Advanced](#advanced)

---

<a name="basic"></a>
### Basic
One level deep menu.
{% raw %}
```
<!--Check the website hierarchy exists-->
{% if Hierarchy['WEB-HIERARCHY-CODE'] %}
	<ul>
	<!--Create a loop of all of the level one nodes-->
	{% for link in Hierarchy['WEB-HIERARCHY-CODE'].HierarchyNodes %}
		<!--Output a link and the description for each node-->
		<li><a href="{{ link.NavigateUrl }}">{{ link.HierarchyLevel.Description}}</a></li>
	{% endfor %}
	<ul>
{% endif %}
```
{% endraw %}

---

<a name="advanced"></a>
### Advanced
Nested menu.
{% raw %}
```
{% if Hierarchy['WEB-HIERARCHY-CODE'] %}
	<ul>
	{% for link in Hierarchy['WEB-HIERARCHY-CODE'].HierarchyNodes %}
		{% if link.HierarchyNodes %}
			<li><a href="{{ link.NavigateUrl }}">{{ link.HierarchyLevel.Description}}</a>
				<ul>
				<!--Create a loop of all of the level two nodes-->
				{% for sublink in link.HierarchyNodes %}
					<!--Output a link and the description for each node-->
					<li><a href="{{ sublink.NavigateUrl }}">{{ sublink.HierarchyLevel.Description}}</a></li>
				{% endfor %}
				</ul>
			</li>
			{% else %}
			<li><a href="{{ link.NavigateUrl }}">{{ link.HierarchyLevel.Description}}</a></li>
		{% endif %}
	{% endfor %}
	<ul>
{% endif %}
```
{% endraw %}

---