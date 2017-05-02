---
layout: collection
title: Communication
name: communication
description: Describes a communication defined by a communication type, details and a password where details can be an email address, a telephone number or any other information.
 
---

## Communication

* [CommunicationType](#communicationtype)
* [Details](#details)
* [Password](#password)

---

<a name="communicationtype"></a>
### CommunicationType
Determines the type of the communication.

{% raw %}
```liquid
{{ Communication.CommunicationType }}

```
{% endraw %}

Data Type: CommunicationType Model

__link to CommunicationType Model__

---

<a name="details"></a>
### Details
Determines the communication details.

{% raw %}
```liquid
{{ Communication.Details }}

```
{% endraw %}

Data Type: string

---

<a name="password"></a>
### Password
Determines the chosen password. This field will only be populated if the communication type is email.

{% raw %}
```liquid
{{ Communication.Password }}

```
{% endraw %}

Data Type: string

---