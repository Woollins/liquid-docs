---
layout: collection
title: UserSetting
name: usersetting
description: An example of a User Setting could be the selected Product Listing template. 
 
---

## UserSetting

* [Name](#name)
* [Value](#value)

---

<a name="name"></a>
### Name
Determines the name of the User Setting.

{% raw %}
```liquid
{{ UserSetting.Name }}

```
{% endraw %}

Data Type: string

---

<a name="value"></a>
### Value
Determines the value of the User Setting. e.g. "grid" for a Setting Name of "list-view"

{% raw %}
```liquid
{{ UserSetting.Value }}

```
{% endraw %}

Data Type: string

---