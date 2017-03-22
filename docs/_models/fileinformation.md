---
layout: collection
title: FileInformation
name: fileinformation
description: Stores an information about the file.
 
---

## FileInformation

* [FileName](#filename)
* [FilePath](#filepath)

---

<a name="filename"></a>
### FileName
Determines the name of a file.

{% raw %}
```liquid
{{ FileInformation.FileName }}

```
{% endraw %}

Data Type: string

---

<a name="filepath"></a>
### FilePath
Determines the path to access a file.

{% raw %}
```liquid
{{ FileInformation.FilePath }}

```
{% endraw %}

Data Type: string

---