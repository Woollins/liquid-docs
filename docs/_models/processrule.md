---
layout: collection
title: ProcessRule
name: processrule
description: Stores details on a Process Rule.
 
---

## ProcessRule

* [ConfirmTransactionDate](#confirmtransactiondate)
* [Description](#description)
* [Visibility](#visibility)
* [WorkflowStageIdForToStage](#workflowstageidfortostage)

---

<a name="confirmtransactiondate"></a>
### ConfirmTransactionDate
Determines whether to confirm transaction date when Processing.

{% raw %}
```liquid
{{ ProcessRule.ConfirmTransactionDate }}

```
{% endraw %}

Data Type: boolean

---

<a name="description"></a>
### Description
Determines the Description of the process rule

{% raw %}
```liquid
{{ ProcessRule.Description }}

```
{% endraw %}

Data Type: string

---

<a name="visibility"></a>
### Visibility
Defines the visibility of the Process Rule.

{% raw %}
```liquid
{{ ProcessRule.Visibility }}

```
{% endraw %}

Data Type: Process Rule Visbility Model

__link to the Process Rule Visbility Model__

---

<a name="workflowstageidfortostage"></a>
### WorkflowStageIdForToStage
Defines the Id of the stage to process to.

{% raw %}
```liquid
{{ ProcessRule.WorkflowStageIdForToStage }}

```
{% endraw %}

Data Type: int

---