---
layout: collection
title: Multi Facet
name: facets
description: Blueprint for displaying refine search section on product listing page.
---

### Multi Facet

EaSearch must be setup within 3ex.net before Facets can be displayed, once it is setup create a partial named "PARTIAL.FACET". Enter the code below.

<div class="example-title">PARTIAL.FACET</div>
{% raw %}
```liquid
<button class="filter-reset-all">Reset All</button>
<ul class="multi-facet">
{% for facet in Facets %}
    {% if facet.Collapsible == 1 %}
    <li class="collapse">
    {% else %}
    <li>
    {% endif %}
        <div class="{{facet.Code}} facet-item" id="{{facet.Code}}" data-filter="{{facet.Code}}" data-filter-type="{{facet.DisplayAs.Type}}">
            <button class="filter-reset">Reset</button>
            <h5>{{facet.Description}}<span class="toggle"></span></h5>
            <div class="facet-items">
            {% if facet.DisplayAs.IsCheckBox %}
                {% for item in facet.FacetItems %}
                    <div class="checkbox {{item.Code}}">
                        <input data-filter-item="{{item.Code}}" id="{{facet.Code}}{{item.Code}}" type="checkbox" {% if item.IsSelected %}checked{% endif %} name="{{facet.Code}}" value="{{item.Code}}">
                         <label for="{{facet.Code}}{{item.Code}}" class="facet-label">{{item.Description}} <span class="facet-title">({{facet.Description}})</span><span>({{item.Count}})</span></label>
                    </div>
                {% endfor %}
            {% elsif facet.DisplayAs.IsValueRangeSlider %}
                <div class="priceSlide">
                    <label class="slider-range-info">{{facet.SelectedValueFrom | FormatCurrency : ActiveCurrency}} - {{facet.SelectedValueTo | FormatCurrency : ActiveCurrency }}</label>
                    <input type="hidden" data-filter-min value="{{facet.SelectedValueFrom}}">
                    <input type="hidden" data-filter-max value="{{facet.SelectedValueTo}}">
                    <label class="slider-selected-range"></label>
                    <div class="slider-range" data-min-value="{{facet.MinimumValue}}" data-max-value="{{facet.MaximumValue}}" data-selected-value-from="{{facet.SelectedValueFrom}}" data-selected-value-to="{{facet.SelectedValueTo}}"></div>
                </div>
            {% elsif facet.DisplayAs.IsComboBox %}
                <select>
                    {% for item in facet.FacetItems %}
                        <option {% if item.IsSelected %}checked{% endif %} value="{{item.Code}}">{{item.Description}} ({{item.Count}})</option>
                    {% endfor %}>
                </select>
            {% endif %}
            </div>
        </div>
    </li>
{% endfor %}
</ul>
```
{% endraw %}

<div class="example-title">Include Facets on listing or search page</div>
{% raw %}
```html
{% if Facets %}
<div id="filters">
    {% include "PARTIAL.FACET" %}
</div>
{% endif %}
```
{% endraw %}