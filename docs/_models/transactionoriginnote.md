---
layout: collection
title: TransactionOriginNote
name: transactionoriginnote
description: Stores details on a Process Rule.
 
---

## TransactionOriginNote

* [CreatedBy](#createdby)
* [DateCreated](#datecreated)
* [Notes](#notes)

---

<a name="createdby"></a>
### CreatedBy
Determines the user that created the Note.

{% raw %}
```liquid
{{ TransactionOriginNote.CreatedBy }}

```
{% endraw %}

Data Type: string

---

<a name="datecreated"></a>
### DateCreated
Determines when the Note was created

{% raw %}
```liquid
{{ TransactionOriginNote.DateCreated }}

```
{% endraw %}

Data Type: DateTime

---

<a name="notes"></a>
### Notes
Determines the Note contents.

{% raw %}
```liquid
{{ TransactionOriginNote.Notes }}

```
{% endraw %}

Data Type: string

---