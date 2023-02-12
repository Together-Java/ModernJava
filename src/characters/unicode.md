# Unicode

Most letters and symbols that are common in the English speaking world fit into
a single `char`, so pretending that a `char` is always "a single
letter or symbol" is generally a good enough mental model.

Where this falls apart is with things like emoji (👨‍🍳) which are generally considered to be one symbol, but 
cannot be represented in a single `char`.

```java
char chef = '👨‍🍳';
```

`char`s are actually "utf-16 code units". Many symbols require multiple "code units" to represent.

For a full explanation, refer to this old Computerphile video. 

It describes "utf-8", which is 8 bits per "code unit." Java's `char`
uses 16 bits, but that is the only difference.

<iframe width="560" height="315" src="https://www.youtube.com/embed/MijmeoH9LT4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


