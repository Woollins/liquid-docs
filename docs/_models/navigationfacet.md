---
layout: collection
title: NavigationFacet
name: navigationfacet
description: Represents a Navigation Facet and how it should be configured. 
 
---

## NavigationFacet

* [CategoryIdForHorizontalMatrix](#categoryidforhorizontalmatrix)
* [CategoryIdForVerticalMatrix](#categoryidforverticalmatrix)
* [Code](#code)
* [Collapsible](#collapsible)
* [Description](#description)
* [DisplayAs](#displayas)
* [FacetItems](#facetitems)
* [MaximumValue](#maximumvalue)
* [MinimumValue](#minimumvalue)
* [SelectedValueFrom](#selectedvaluefrom)
* [SelectedValueTo](#selectedvalueto)
* [SortBy](#sortby)
* [SortOrder](#sortorder)
* [TypeOfPrice](#typeofprice)
* [ValuePrefix](#valueprefix)
* [ValueSuffix](#valuesuffix)

---

<a name="categoryidforhorizontalmatrix"></a>
### CategoryIdForHorizontalMatrix
Determines the Category Id For Horizontal Matrix.

{% raw %}
```liquid
{{ NavigationFacet.CategoryIdForHorizontalMatrix }}

```
{% endraw %}

Data Type: int

---

<a name="categoryidforverticalmatrix"></a>
### CategoryIdForVerticalMatrix
Determines the Category Id For Vertical Matrix.

{% raw %}
```liquid
{{ NavigationFacet.CategoryIdForVerticalMatrix }}

```
{% endraw %}

Data Type: int

---

<a name="code"></a>
### Code
Determines the Navigation Facet Item code.

{% raw %}
```liquid
{{ NavigationFacet.Code }}

```
{% endraw %}

Data Type: string

---

<a name="collapsible"></a>
### Collapsible
Determines the whether or not the Facet Item is collapsible and if it should be expanded if it is.

{% raw %}
```liquid
{{ NavigationFacet.Collapsible }}

```
{% endraw %}

Data Type: byte

---

<a name="description"></a>
### Description
Determines the facet name/description.

{% raw %}
```liquid
{{ NavigationFacet.Description }}

```
{% endraw %}

Data Type: string

---

<a name="displayas"></a>
### DisplayAs
Determines what to display the Facet Item as e.g. check box, combo box, etc.

{% raw %}
```liquid
{{ NavigationFacet.DisplayAs }}

```
{% endraw %}

Data Type: NavigationFacetDisplayAs Model

__link to NavigationFacetDisplayAs Model__

---

<a name="facetitems"></a>
### FacetItems
An array of Navigation Facet Items to be rendered for the current Navigation Facet. E.g. For a Navigation Facet of colour, this array would contain values such as "Red", "Blue", "Green" etc.

{% raw %}
```liquid
{{ NavigationFacet.FacetItems }}

```
{% endraw %}

Data Type: NavigationFacetItem Model	

__link to NavigationFacetItem Model	__

---

<a name="maximumvalue"></a>
### MaximumValue
Determines where the facet style is configured as a range (eg Price), this holds the maximum value.

{% raw %}
```liquid
{{ NavigationFacet.MaximumValue }}

```
{% endraw %}

Data Type: decimal	

---

<a name="minimumvalue"></a>
### MinimumValue
Determines where the facet style is configured as a range (eg Price), this holds the minimum value.

{% raw %}
```liquid
{{ NavigationFacet.MinimumValue }}

```
{% endraw %}

Data Type: decimal	

---

<a name="selectedvaluefrom"></a>
### SelectedValueFrom
Determines where the facet style is configured as a range (eg Price), this holds the from value that the user originally selected when they performed a search.

{% raw %}
```liquid
{{ NavigationFacet.SelectedValueFrom }}

```
{% endraw %}

Data Type: decimal	

---

<a name="selectedvalueto"></a>
### SelectedValueTo
Determines where the facet style is configured as a range (eg Price), this holds the to value that the user originally selected when they performed a search.

{% raw %}
```liquid
{{ NavigationFacet.SelectedValueTo }}

```
{% endraw %}

Data Type: decimal	

---

<a name="sortby"></a>
### SortBy
Determines the sort by type e.g. ascending, descending, A-Z, etc.

{% raw %}
```liquid
{{ NavigationFacet.SortBy }}

```
{% endraw %}

Data Type: byte	

---

<a name="sortorder"></a>
### SortOrder
Determines the order in which the item should appear for the current hierarchy.

{% raw %}
```liquid
{{ NavigationFacet.SortOrder }}

```
{% endraw %}

Data Type: int	

---

<a name="typeofprice"></a>
### TypeOfPrice
Defines how the price field should be interpreted e.g. Use VAT Inclusive, VAT Exclusive, etc.

{% raw %}
```liquid
{{ NavigationFacet.TypeOfPrice }}

```
{% endraw %}

Data Type: byte	

---

<a name="valueprefix"></a>
### ValuePrefix
Can be used to prefix the facet values in the UI, eg with a currency code or unit of measure such as mm, kg etc.

{% raw %}
```liquid
{{ NavigationFacet.ValuePrefix }}

```
{% endraw %}

Data Type: string

---

<a name="valuesuffix"></a>
### ValueSuffix
Can be used to suffix the facet values in the UI, eg with a currency code or unit of measure such as mm, kg etc.

{% raw %}
```liquid
{{ NavigationFacet.ValueSuffix }}

```
{% endraw %}

Data Type: string

---