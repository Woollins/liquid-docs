---
layout: normal
title: EA Search Bar
name: ea-search-bar
description: Allows customers to search your site quickly, by product name, code, search term.
category: navigation
---

## EA Search Bar
Usually positioned within the header of the website the search feature enables users to quickly search for products. A drop down for search suggestions can also be implemented to aid the users search.

<div class="example-title">HTML / Liquid</div>
{% raw %}
```liquid
<div class="search small-12 medium-6 large-4 columns">
    <div id="search-bar">
        <form class="search__form" > 
           <input autocomplete="off" title="Numbers & letters only" id="search-text" class="search__form--text" pattern="[a-z\d\-]*" name="SearchTermParameterName" type="search" placeholder="Search keyword or product code" />
           <button aria-label="Search" id="header-search-button" type="submit" class="search__form--button"><i class="fa fa-search"></i></button>
        </form>
        <div id="searchSuggestion" style="display:none;">
    </div>
</div>
```
{% endraw %}

<div class="example-title">SCSS</div>
{% raw %}
```scss

```
{% endraw %}

__Include SCSS - will also need a link to the search results page__