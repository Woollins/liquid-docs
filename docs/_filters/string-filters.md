---
layout: collection
title: String Filters
name: string-filters
description: manipulate outputs and variables
---

**String Filters**
String filters are used to manipulate outputs and variables.

* [Append](#append)
* [Capitalize](#capitalize)
* [Downcase](#downcase) 
* [NewlineToBr](#newlinetobr) 
* [Prepend](#prepend) 
* [Remove](#remove) 
* [RemoveFirst](#removefirst) 
* [Replace](#replace) 
* [ReplaceFirst](#replacefirst) 
* [Slice](#slice)
* [Split](#split)
* [Truncate](#truncate)
* [Truncatewords](#truncatewords)
* [Upcase](#upcase)


<a name="append"></a>
### Append 
Add one sting to another
{% raw %}
```liquid
{{ Product.Description | Append: " (SALE!)" }}
```
{% endraw %}
Output: 'Awesome Shoes (SALE!)''

<a name="capitalize"></a>
### Capitalize 
Converts the first character of a string top uppercase.
{% raw %}
```liquid
{{ "my great title" | Capitalize }}
```
{% endraw %}
'capitalize' only capitalizes the first character of the string, so later words are not affected. Output: 'My great title'

<a name="downcase"></a>
### Downcase 
Converts a string to lowercase
{% raw %}
```liquid
{{ "My Great TiTLe" | Downcase }}
```
{% endraw %}
Output: 'my great title'

<a name="newlinetobr"></a>
### NewlineToBr 
Adds {% raw %}<br />{% endraw %} tags in front of all newlines in input string.
Product Specification: 
2005, Hatchback, 
59.000 miles, 
Manual, 1.6L, Diesel
{% raw %}
```liquid
{{ Product["Answer_SPECIFICATION"] | NewlineToBr }}
```
{% endraw %}
Output: '2005, Hatchback,{% raw %}<br />{% endraw %}  59.000 miles, Manual,{% raw %}<br />{% endraw %}  1.6L, Diesel'

<a name="prepend"></a>
### Prepend 
Prepend a string to another
{% raw %}
```liquid
{{ "Awesome Shoes" | Prepend: "(SALE!) " }}
```
{% endraw %}
Output: '(SALE!) Awesome Shoes'

<a name="remove"></a>
### Remove 
Remove a substring.
{% raw %}
```liquid
{{ "These awesome shoes are really awesome" | Remove: "awesome" }}
```
{% endraw %}
Output: 'These Shoes are really'

<a name="removefirst"></a>
### RemoveFirst 
Remove the first occurrence of a substring.
{% raw %}
```liquid
{{ "These awesome shoes are really awesome" | Remove: "Awesome" }}
```
{% endraw %}
Output: 'These shoes are really awesome'

<a name="replace"></a>
### Replace 
Replace occurrences of a string with another.
{% raw %}
```liquid
{{ "These awesome shoes are really awesome" | Replace : "These", "My" }}
```
{% endraw %}
Output: 'My awesome shoes are really awesome'

<a name="replacefirst"></a>
### ReplaceFirst 
Replace the first occurence of a string with another.
{% raw %}
```liquid
{{ "These awesome shoes are really awesome" | ReplaceFirst : "awesome", "great" }}
```
{% endraw %}
Output: 'These great shoes are really awesome'

<a name="slice"></a>
### Slice 
Returns a part of a string, starting at the specified index.  A second parameter can be passed to specify the length of the string. If the second parameter is not specified a string of one character will be returned.  (Note: Strings are numbered starting from 0)
{% raw %}
```liquid
{{ "hello" | Slice: 0 }}
```
{% endraw %}
Output: 'h'
{% raw %}
```liquid
{{ "hello" | Slice: 1 }}
```
{% endraw %}
Output: 'e'
{% raw %}
```liquid
{{ "hello" | Slice: 1, 3 }}
```
{% endraw %}
Output: 'ell'

If the passed index is negative, it is counted from the end of the string.
{% raw %}
```liquid
{{ "hello" | Slice: -3, 2  }}
```
{% endraw %}
Output: 'll'

<a name="split"></a>
### Split 
Split an input string into an array of substrings separated by given pattern. 
{% raw %}
```liquid
{% "Hi, how are you today?" | Split: ' ' %}
```
{% endraw %}
Output:
'
Hi,
how
are
you
today?
'

<a name="truncate"></a>
### Truncate 
Truncates a string down to specific amount of characters.
{% raw %}
```liquid
{{ "Hi, how are you today?" | Truncate : 10 }}
```
{% endraw %}
Output: 'Hi, how ar...''

'Truncate' takes an optional second parameter that specifies the sequence of characters to be appended to the truncated string. By default this is an ellipsis (...), but you can specify a different sequence.

The length of the second parameter counts against the number of characters specified by the first parameter. For example, if you want to truncate a string to exactly 10 characters, and use a 3-character ellipsis, use 13 for the first parameter of truncate, since the ellipsis counts as 3 characters.
{% raw %}
```liquid
{{ "Hi, how are you today?" | Truncate : 11, '?' }}
```
{% endraw %}
Output: 'Hi, how ar?''

<a name="truncatewords"></a>
### Truncatewords 
Truncates a string down to specific amount of words.
{% raw %}
```liquid
{{ "Hi, how are you today?" | TruncateWords : 1 }}
```
{% endraw %}
Output: 'Hi'

'Truncatewords' takes an optional second parameter that specifies the sequence of characters to be appended to the truncated string. By default this is an ellipsis (…), but you can specify a different sequence.
{% raw %}
```liquid
{{ "Hi, how are you today?" | TruncateWords : 1 , '!'}}
```
{% endraw %}
Output: 'Hi!'

You can avoid showing trailing characters by passing a blank string as the second parameter:
{% raw %}
```liquid
{{ "Hi, how are you today?" | TruncateWords : 1 , ''}}
```
{% endraw %}
Output: 'Hi'

<a name="upcase"></a>
### Upcase 
Converts a string to uppercase
{% raw %}
```liquid
{{ "Hello" | Upcase }}
```
{% endraw %}
Output: 'HELLO'


