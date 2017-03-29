---
layout: collection
title: Search Form
name: search
description: Blueprint for displaying the search form on your website.
---

### Breadcrumbs

<div class="example-title">Input</div>
{% raw %}
```liquid
<div id="search-bar">
    <form class="search-form" > 
       <input autocomplete="off" title="Numbers & letters only" id="search-text" class="search-text" pattern="[a-z\d\-]*" name="SearchTermParameterName" type="search" placeholder="Keyword or product code" />
       <button id="header-search-button" type="submit" class="search show-for-large">Search</button>
    </form>
</div>

```
{% endraw %}