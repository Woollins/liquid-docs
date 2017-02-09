---
layout: collection
title: String Filters
---

## String Filters
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
```
{{ Product.Description | Append: " (SALE!)" }}
```
Output: ```Awesome Shoes (SALE!)```

<a name="capitalize"></a>
### Capitalize 
Converts the first character of a string top uppercase.
```
{{ "my great title" | Capitalize }}
```
```capitalize``` only capitalizes the first character of the string, so later words are not affected. Output: ```My great title```

<a name="downcase"></a>
### Downcase 
Converts a string to lowercase
```
{{ "My Great TiTLe" | Downcase }}
```
Output: ```my great title```

<a name="newlinetobr"></a>
### NewlineToBr 
Adds <br /> tags in front of all newlines in input string.
Product Specification: 
2005, Hatchback, 
59.000 miles, 
Manual, 1.6L, Diesel
```
{{ Product["Answer_SPECIFICATION"] | NewlineToBr }}
```
Output: ```2005, Hatchback,<br />  59.000 miles, Manual,<br />  1.6L, Diesel```

<a name="prepend"></a>
### Prepend 
Prepend a string to another
```
{{ "Awesome Shoes" | Prepend: "(SALE!) " }}
```
Output: ```(SALE!) Awesome Shoes```

<a name="remove"></a>
### Remove 
Remove a substring.
```
{{ "These awesome shoes are really awesome" | Remove: "awesome" }}
```
Output: ```These Shoes are really```

<a name="removefirst"></a>
### RemoveFirst 
Remove the first occurrence of a substring.
```
{{ "These awesome shoes are really awesome" | Remove: "Awesome" }}
```
Output: ```These shoes are really awesome```

<a name="replace"></a>
### Replace 
Replace occurrences of a string with another.
```
{{ "These awesome shoes are really awesome" | Replace : "These", "My" }}
```
Output: ```My awesome shoes are really awesome```

<a name="replacefirst"></a>
### ReplaceFirst 
Replace the first occurence of a string with another.
```
{{ "These awesome shoes are really awesome" | ReplaceFirst : "awesome", "great" }}
```
Output: ```These great shoes are really awesome```

<a name="slice"></a>
### Slice 
Returns a part of a string, starting at the specified index.  A second parameter can be passed to specify the length of the string. If the second parameter is not specified a string of one character will be returned.  (Note: Strings are numbered starting from 0)
```
{{ "hello" | Slice: 0 }}
```
Output: ```h``````
```
{{ "hello" | Slice: 1 }}
```
Output: ```e```
```
{{ "hello" | Slice: 1, 3 }}
```
Output: ```ell```

If the passed index is negative, it is counted from the end of the string.
```
{{ "hello" | Slice: -3, 2  }}
```
Output: ```ll```

<a name="split"></a>
### Split 
Split an input string into an array of substrings separated by given pattern. 
```
{% raw %}{% "Hi, how are you today?" | Split: ' ' %}{% endraw %}
```
Output:
```
Hi,
how
are
you
today?
```

<a name="truncate"></a>
### Truncate 
Truncates a string down to specific amount of characters.
```
{{ "Hi, how are you today?" | Truncate : 10 }}
```
Output: ```Hi, how ar...```

```Truncate``` takes an optional second parameter that specifies the sequence of characters to be appended to the truncated string. By default this is an ellipsis (...), but you can specify a different sequence.

The length of the second parameter counts against the number of characters specified by the first parameter. For example, if you want to truncate a string to exactly 10 characters, and use a 3-character ellipsis, use 13 for the first parameter of truncate, since the ellipsis counts as 3 characters.

```
{{ "Hi, how are you today?" | Truncate : 11, '?' }}
```
Output: ```Hi, how ar?```

<a name="truncatewords"></a>
### Truncatewords 
Truncates a string down to specific amount of words.
```
{{ "Hi, how are you today?" | TruncateWords : 1 }}
```
Output: ```Hi```

```Truncatewords``` takes an optional second parameter that specifies the sequence of characters to be appended to the truncated string. By default this is an ellipsis (…), but you can specify a different sequence.

```
{{ "Hi, how are you today?" | TruncateWords : 1 , '!'}}
```
Output: ```Hi!```

You can avoid showing trailing characters by passing a blank string as the second parameter:
```
{{ "Hi, how are you today?" | TruncateWords : 1 , ''}}
```
Output: ```Hi```

<a name="upcase"></a>
### Upcase 
Converts a string to uppercase
```
{{ "Hello" | Upcase }}
```
Output: ```HELLO```