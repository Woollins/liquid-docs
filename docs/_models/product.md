---
layout: collection
title: Product
name: product
description: is used to access the properties of the products within your shop
---


**The Product Model** is used to access the details of the products within your shop.  The Product model has the following attributes:

* [Code](#code)
* [CodeToUseInUrl](#codetouseinurl)
* [Id](#id)
* [Description](#description)
* [DescriptionToUseInUrl](#descriptiontouseinurl)
* [NavigateUrl](#navigateurl)
* [Additional Fields](#additional)
* [DefaultHierarchyNodeModel](#default)
* [ProductPrice](#price)
* [ProductPrices](#prices)
* [FormOfProduct](#formofproduct)
* [MetadataForOverride](#metadataforoverride)
* [ProductGroupCodeForSegmentation](#segmentation)
* [Tags](#tags)

---

<a name="code"></a>
### Code
Returns the product code that has been set against the product within the 3ex.net system.
{% raw %}
```liquid
{{ Product.Code }}
```
{% endraw %}

---

<a name="codetouseinurl"></a>
### CodeToUseInUrl	
Similar to the Code, but with illegal URL characters removed to make it suitable for use in hyperlinks.
{% raw %}
```liquid
{{ Product.CodeToUseInUrl }}
```
{% endraw %}

---

<a name="id"></a>
### Id
This will return the unique id of a product.
{% raw %}
```liquid
{{ Product.Id }}
```
{% endraw %}

---

<a name="description"></a>
### Description
A brief description of the product will be returned.
{% raw %}
```liquid
{{ Product.Description }}
```
{% endraw %}

---

<a name="descriptiontouseinurl"></a>
### DescriptionToUseInUrl	
Similar to the Description, but with illegal URL characters removed to make it suitable for use in hyperlinks.
{% raw %}
```liquid
{{ Product.DescriptionToUseInUrl }}
```
{% endraw %}

---

<a name="navigateurl"></a>
### NavigateUrl
This will return a url that a website visitor can click to take them to the product detail page for the product.
{% raw %}
```liquid 
<a href="{{ Product.NavigateUrl }}">{{ Product.Description }}</a>
```
{% endraw %}

---

<a name="default"></a>
### DefaultHierarchyNodeModel	
Holds the Default Hierarchy Node data if it's available. The DefaultHierarchyNode is the default hierarchy that gets assigned to a product. This gives you access to all the HierachyNode attributes for the Products default HierarchyNode.
{% raw %}
```liquid
{{ Product.DefaultHierarchyNodeModel.NavigateUrl }}
```
{% endraw %}

Output: This will generate the url for the Products Default HierarchyNode.

**__For a list of all HierarchyNode attributes see here - create link__** 

---

<a name="price"></a>
### ProductPrice	
Contains pricing information for the default Vertical price matrix.
{% raw %}
```liquid
{{ Product.StandardOurPrice_VatInclusivePrice }}
{{ Product.StandardOurPrice_VatExclusivePrice }}
{{ Product.WasPrice_VatInclusivePrice }}
```
{% endraw %}

**__Will need to update this once standard has been agreed - will need to link through to the Product Price	Model__** 

---

<a name="prices"></a>
### ProductPrices	
Allows pricing information to be queried via a code.

{% raw %}
```liquid
{{ Product.StandardOurPrice_VatInclusivePrice }}
{{ Product.StandardOurPrice_VatExclusivePrice }}
{{ Product.WasPrice_VatInclusivePrice }}
```
{% endraw %}

**__Need to explain a bit more about what this is__**

**__Will need to update this once standard has been agreed - will need to link through to the Product Price	Model__** 

---

<a name="formofproduct"></a>
### FormOfProduct	
Used to determine what the type of product is.  The FormOfProduct is the type that is assigned to a Product when it is set up.  
{% raw %}
```liquid
{{ Product.FormOfProduct.IsVariantBase }}
```
{% endraw %}

This above example could be used within an if statement to render certain information only for a product if it is a base variant product.

**__For a list of all FormOfProduct attributes see here - create link__** 

---

<a name="metadataforoverride"></a>
### MetadataForOverride		
The Override Metadata for this Product if any exists.
{% raw %}
```liquid
{{ Page.MetaDescription }}
```
{% endraw %}

**__Need to explain a bit more about what this is__**

---

<a name="segmentation"></a>
### ProductGroupCodeForSegmentation	
Product Group Code to use for segmentation.

**__Need to explain a bit more about what this is (I don't know)__**

---

<a name="tags"></a>
### Tag
This will return the website Tag for a Product.
{% raw %}
```liquid
{{ Tag.TagName }}
```
{% endraw %}
Output: This will return the Name of the Tag.

**__For a list of all Tag attributes see here - create link__** 

---

<a name="additional"></a>
### Additional Fields
Within the Product model you can access additional data set against the product. Related Data elements are used to store extra information that you may want to display, for example a products short description.
{% raw %}
```liquid
{{ Product.Answer_PSD }}
{{ Product.Answer_C1 }}
{{ Product.Answer_C2 }}
{{ Product.Answer_C3 }}
```
{% endraw %}

Output: Product Short Description, Characterstic One, Characterstic Two, Characterstic Three

**__This will need more detail when standard has been agreed__**
