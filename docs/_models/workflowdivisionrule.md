---
layout: collection
title: WorkflowDivisionRule
name: workflowdivisionrule
description: Holds Workflow Division Rule information for the currently active company division
 
---

## WorkflowDivisionRule

* [AddressTypeIdForDeliveryAddress](#addresstypeidfordeliveryaddress)
* [AddressTypeIdForPrimaryAddress](#addresstypeidforprimaryaddress)
* [CompanyDivisionId](#companydivisionid)
* [ExtractCategoryFromProductSearch](#extractcategoryfromproductsearch)
* [OtherAddressTypeIds](#otheraddresstypeids)
* [WorkflowId](#workflowid)

---

<a name="addresstypeidfordeliveryaddress"></a>
### AddressTypeIdForDeliveryAddress
Determines the Address Type Id to use for delivery addresses.

{% raw %}
```liquid
{{ WorkflowDivisionRule.AddressTypeIdForDeliveryAddress }}

```
{% endraw %}

Data Type: int

---

<a name="addresstypeidforprimaryaddress"></a>
### AddressTypeIdForPrimaryAddress
Determines the Address Type Id to use for primary addresses.

{% raw %}
```liquid
{{ WorkflowDivisionRule.AddressTypeIdForPrimaryAddress }}

```
{% endraw %}

Data Type: int

---

<a name="companydivisionid"></a>
### CompanyDivisionId
Determines the Id of the Company Division the Workflow Division Rule row belongs to.

{% raw %}
```liquid
{{ WorkflowDivisionRule.CompanyDivisionId }}

```
{% endraw %}

Data Type: int

---

<a name="extractcategoryfromproductsearch"></a>
### ExtractCategoryFromProductSearch
Determines whether to extract the category from the product search.

{% raw %}
```liquid
{{ WorkflowDivisionRule.ExtractCategoryFromProductSearch }}

```
{% endraw %}

Data Type: boolean

---
	
<a name="otheraddresstypeids"></a>
### OtherAddressTypeIds
Determines other address type Ids in an array.

{% raw %}
```liquid
{{ WorkflowDivisionRule.OtherAddressTypeIds }}

```
{% endraw %}

Data Type: int

---

<a name="workflowid"></a>
### WorkflowId
Determines the Id of the associated work flow.

{% raw %}
```liquid
{{ WorkflowDivisionRule.WorkflowId }}

```
{% endraw %}

Data Type: int

---