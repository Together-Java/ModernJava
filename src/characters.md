# Characters

A character, represented by the data type `char`, is a "utf-16 unicode codepoint". 

```java
char letter = 'a';
```

Most letters and symbols that are common in the English speaking world fit into
a single `char`, and that is a generally good way to think about it. A `char` is a single
letter or symbol.

Where this mental model falls apart is with things like emoji (🤗) which are generally considered to be one symbol, but require
multiple "unicode codepoints" to represent.

<!-- TODO: Better explanation + Don't shell out to youtube video. -->

For a full explanation, refer to this old Computerphile video. 

It describes "utf-8", which is 8 bits per "unicode codepoint." Java's `char`
uses 16 bits.


<iframe width="560" height="315" src="https://www.youtube.com/embed/MijmeoH9LT4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
