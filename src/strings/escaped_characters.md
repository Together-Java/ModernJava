# Escaped Characters

Inside of a string literal, there are some characters that cannot be written normally.


An easy example is double quotes. You can't write double quotes in the middle of
a string literal because Java will think the extra quote is the end of the `String`.

```java
String title = "The "Honorable" Judge Judy";
```

In order to make it work, the `"`s need to be "escaped" with a backslash.

```java
String title = "The \"Honorable\" Judge Judy";
```

Since the backslash is used to escape characters, it too needs to escaped
in order to have it be in a `String`. So to encode `¯\_(ツ)_/¯` into a String
you need to escape the first backslash.

```java
// The first backslash needs to be escaped. ¯\_(ツ)_/¯
String shruggie = "¯\\_(ツ)_/¯";
```

