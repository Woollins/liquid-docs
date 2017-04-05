---
layout: collection
title: Content Managed Regions
name: content-managed-regions
description: Blueprint for adding content managed regions to a page.
---

**Content Managed Regions** 

<div class="example-title">Create a new physical page for product listing and add the following code.</div>
{% raw %}
```liquid
{{ ContentManagedRegion["CMR-CODE"].Segments["SEGMENT NAME"].Contents | Prepend: '<div>' | Append: '</div>' }}
```
{% endraw %}

