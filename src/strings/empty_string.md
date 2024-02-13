# The Empty String

There is a special `String` which contains no characters at all.

```java
~void main() {
// There is nothing to say.
String conversationWithDog = "";
~}
```

You write it just like any other string, just with nothing between the double quotes.

```java,no_run
""
```

It is different from a `String` that just contains spaces because to Java those "space characters"
are just as much real characters as `a`, `b`, or `c`.

```java
~void main() {
// There is noteworthy silence.
String conversationWithInlaws = " ";
~}
```

This is one of those things that feels totally useless, but comes in handy pretty often.

- Say you are writing a message to send to your friend. The messenger
  app can represent the state of the input box before you type anything with
  an empty `String`.
- If you want to digitally record responses to legal paperwork, you might choose
  to represent skipped fields as empty `String`s.
- Video Games where characters have assigned names can assign an empty `String`
  as the name of otherwise "unnamed" characters.
- etc.
