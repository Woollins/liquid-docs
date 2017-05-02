---
layout: collection
title: ThemeAdvancedRule
name: themeadvancedrule
description: A rule that can be applied to control certain behaviour or logic within the theme. The value of the rule is obtained by using the RuleName to look it up in the model dictionary.  
 
---

## ThemeAdvancedRule

* [RuleName](#rulename)
* [RuleValue](#rulevalue)

---

<a name="rulename"></a>
### RuleName
Determines the name of the rule.

{% raw %}
```liquid
{{ ThemeAdvancedRule.RuleName }}

```
{% endraw %}

Data Type: string

---

<a name="rulevalue"></a>
### RuleValue
Determines the value of the rule

{% raw %}
```liquid
{{ ThemeAdvancedRule.RuleValue }}

```
{% endraw %}

In the below example we will display the mini basket if the value is true.

{% raw %}
```liquid
{% if ThemeAdvancedRule["UseMiniBasket"].RuleValue == "true" %}

```
{% endraw %}

Data Type: string

---