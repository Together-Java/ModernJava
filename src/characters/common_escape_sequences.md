# Common Escape Sequences

While most characters can be written directly into a program, as is the
case for `a`, `b`, or `t`, there are some which cannot.

For these, you need to use what is called an "escape sequence."

The most common escape sequence you will use will be the one for a "new line."
Which is a backslash followed by an `n`.

```java
char newline = '\n';
```

Because a backslash is used for this special syntax, to put a backslash into a character literal
you need to escape it with a backslash of its own.

```java
char backslash = '\\';
```

And because single quotes are used to mark the start and end of a character literal, they need to be escaped
as well.

```java
char singleQuote = '\'';
```
