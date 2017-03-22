---
layout: collection
title: Error
name: error
description: Provides access to an unhandled exception that might have occurred on the website to allow a custom error page to be rendered.
 
---

## Error

* [Details](#details)
* [Message](#message)
* [Source](#source)

---

<a name="details"></a>
### Details
Full details of the error, including a stack trace.

{% raw %}
```liquid
{{ Error.Details }}

```
{% endraw %}

Data Type: string

---

<a name="message"></a>
### Message
A brief description of the error.

{% raw %}
```liquid
{{ Error.Message }}

```
{% endraw %}

Data Type: string

---

<a name="source"></a>
### Source
Determines the name of the object where the error occured.

{% raw %}
```liquid
{{ Error.Source }}

```
{% endraw %}

Data Type: string

---