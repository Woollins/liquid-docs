---
layout: collection
title: Parameter Parser Element
name: parameterparserelement
description: A parameter parser element will either be of type 'Text' or 'Token'. When the type is 'Text', no additional processing will be required and the raw content will be displayed. If the type is token, the content will be analysed and the appropriate content will be generated.
 
---

## Parameter Parser Element

__this will need more information__

* [Arguments](#arguments)
* [Text](#text)
* [Type](#type)

---

<a name="arguments"></a>
### Arguments
An array of arguments used when generating the controls (label or button) to display.

{% raw %}
```liquid
{{  }}

```
{% endraw %}

Data Type: string array

---

<a name="text"></a>
### Text
Determines the text content to display.

{% raw %}
```liquid
{{  }}

```
{% endraw %}

Data Type: string 

---

<a name="type"></a>
### Type 
Represents the type of content to be displayed. 0 = Text and 1 = Token. Text will be displayed as is and a token will be converted to the appropriate control (e.g. a product label or a product button).

{% raw %}
```liquid
{{  }}

```
{% endraw %}

Data Type: byte

---
			