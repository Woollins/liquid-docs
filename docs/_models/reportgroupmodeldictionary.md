---
layout: collection
title: Report Group Model Dictionary
name: reportgroupmodeldictionary
description: Allows dynamic loading of Report Group Models by Report Group Name
 
---

## Report Group Model Dictionary

The Report Group Name is specified when accessing the dictionary and as long as it is valid the Report Group Model will be returned and populated with Report Groups.

{% raw %}
```liquid
{{ReportGroups["Customer Reports"].Description}}

```
{% endraw %}
