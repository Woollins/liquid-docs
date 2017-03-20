---
layout: collection
title: Hierarchy Node
name: hierarchynode
description: A hierarchy node contains the hierarchy structure.  This can include hierarchy levels, panels as well as other hierarchy nodes.
 
---

## Hierarchy Node

* [ContentManagedPage](#contentmanagedpage)
* [ContentManagedRegion](#contentmanagedregion)
* [DirectLink](#directlink)
* [DisplayAsProductListing](#displayasproductlisting)
* [HierarchyLevel](#hierarchylevel)
* [HierarchyNodePath](#hierarchynodepath)
* [HierarchyNodes](#hierarchynodes)
* [HierarchyPageName](#hierarchypagename)
* [HierarchyPanel](#hierarchypanel)
* [HierarchyPathNodes](#hierarchypathnodes)
* [Id](#id)
* [NavigateUrl](#navigateurl)
* [ProductListingPageName](#productlistingpagename)
* [ProductPageName](#productpagename)
* [Products](#products)
* [ProductSection](#productsection)
* [SortOrder](#sortorder)

---

<a name="contentmanagedpage"></a>
### ContentManagedPage 
If a Content Managed Page is attached to the hierarchy, it's model can be accessed.

{% raw %}
```liquid
{{ HierarchyNode.ContentManagedPage }}

{{ Hierarchy["SHOP"].ContentManagedPage }}

```
{% endraw %}

Data Type: Content Managed Page Model

---

<a name="contentmanagedregion"></a>
### ContentManagedRegion 
If a Content Managed Region is attached to the hierarchy, it's model can be accessed.

{% raw %}
```liquid
{{ HierarchyNode.ContentManagedRegion }}

{{ Hierarchy["SHOP"].ContentManagedRegion.Contents }}

```
{% endraw %}

Data Type: Content Managed Region Model

__mlink to content managed region model__

---

<a name="directlink"></a>
### Direct Link 
If a Direct Link is attached to the hierarchy, it's model can be accessed.

{% raw %}
```liquid
{{ HierarchyNode.DirectLink }}

{{ Hierarchy["SHOP"].irectLink.Description }}

```
{% endraw %}

Data Type: Direct Link Model

__link to direct link model__

---


<a name="displayasproductlisting"></a>
### DisplayAsProductListing
Determines whether the hierachy level should be displayed as a product listing.

{% raw %}
```liquid
{{ HierarchyNode.DisplayAsProductListing }}

```
{% endraw %}

Data Type: boolean

__may need to double check this__

---

<a name="hierarchylevel"></a>
### HierarchyLevel
If a hierarchy level has been attached to the hierarchy, it's model can be accessed.

{% raw %}
```liquid
{{ HierarchyNode.HierarchyLevel }}

```
{% endraw %}

Data Type: Hierarchy Level Model

__need to link to HierarchyLevel__

---

<a name="hierarchynodepath"></a>
### HierarchyNodePath
This will display the path of the hierarchy level.

{% raw %}
```liquid
{{ HierarchyNode.HierarchyNodePath }}

```
{% endraw %}

Data Type: string

__may need more info__

---
	
<a name="hierarchynodes"></a>
### HierarchyNodes
Provides access to to the child elements of the hierarchy.  If the hierarchy does not have any child elements then this will be null.

{% raw %}
```liquid
{{ HierarchyNode.HierarchyNodes }}

```
{% endraw %}

Data Type: Hierarchy Node Model array

__may need more info__

---

<a name="hierarchypagename"></a>
### HierarchyPageName
This can be used to override the default template that is beign used to render the hierarchy page.

{% raw %}
```liquid
{{ HierarchyNode.HierarchyPageName }}

```
{% endraw %}

Data Type: string

__may need more info__

---


<a name="hierarchypanel"></a>
### HierarchyPanel
If a hierarchy panel has been attached to the hierarchy, it's model can be accessed.

{% raw %}
```liquid
{{ HierarchyNode.HierarchyPanel }}

```
{% endraw %}

Data Type: Hierarchy Panel Model

__may need more info - link to Hierarchy Panel Model__

---

<a name="hierarchypathnodes"></a>
### HierarchyPathNodes
Provides access to to the parent elements of the current element within the hierarchy.  This would be used to generate a breadcrumb trail.

{% raw %}
```liquid
{{ HierarchyNode.HierarchyPathNodes }}

```
{% endraw %}

Data Type: Hierarchy Node Model array

__link to Hierarchy Node Model and to blueprints__

---

<a name="id"></a>
### Id
The id can be used to look up a particular hierachy level.

{% raw %}
```liquid
{{ HierarchyNode.Id }}

```
{% endraw %}

Data Type: integer

__more info needed__

---

<a name="navigateurl"></a>
### NavigateUrl
Determines the url to navigate to the hierarchy level.

{% raw %}
```liquid
{{ HierarchyNode.NavigateUrl }}

```
{% endraw %}

Data Type: string

__link to this being used/more info__

---

<a name="productlistingpagename"></a>
### ProductListingPageName
Determines the product listing page name to use for the hiearchy level.

{% raw %}
```liquid
{{ HierarchyNode.ProductListingPageName }}

```
{% endraw %}

Data Type: string

__link to this being used/more info__

---

<a name="productpagename"></a>
### ProductPageName
Determines the product page name to use for the hiearchy level.

{% raw %}
```liquid
{{ HierarchyNode.ProductListingPageName }}

```
{% endraw %}

Data Type: string

__link to this being used/more info__

---

<a name="products"></a>
### Products
When the hierarchy level is defined as a product listing, this property provided access to all the products attached to that hierarchy level.

{% raw %}
```liquid
{{ HierarchyNode.Products }}

```
{% endraw %}

Data Type: Product Model array

__link to Product Model array/more info/blueprint__

---

<a name="productsection"></a>
### ProductSection
Provides access to the product sections that are configured for the current hierarchy level.

{% raw %}
```liquid
{{ HierarchyNode.ProductSection }}

```
{% endraw %}

Data Type: Product Section Model dictionary

__link to Product Section Model/more info/blueprint__

---

<a name="sortorder"></a>
### SortOrder
Determines the position within the parent nodes collection.

{% raw %}
```liquid
{{ HierarchyNode.SortOrder }}

```
{% endraw %}

Data Type: integer

__link to Product Section Model/more info/blueprint__

---

