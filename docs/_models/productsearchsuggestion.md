---
layout: collection
title: ProductSearchSuggestion
name: productsearchsuggestion
description: Contains the results of performing a product search.
 
---

## ProductSearchSuggestion

* [AutoCompletions](#autocompletions)
* [SearchHits](#searchhits)

---

<a name="autocompletions"></a>
### AutoCompletions
Determines the suggested auto completions.

{% raw %}
```liquid
{{ ProductSearchSuggestion.AutoCompletions }}

```
{% endraw %}

Data Type: SearchAutoCompletion Model

__link to SearchAutoCompletion Model__

---

<a name="searchhits"></a>
### SearchHits
Determines hits that were found for the search term.

{% raw %}
```liquid
{{ ProductSearchSuggestion.SearchHits }}

```
{% endraw %}

Data Type: SearchHit Model

__link to SearchHit Model__

---