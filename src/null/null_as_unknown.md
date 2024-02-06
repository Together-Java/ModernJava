# Null as Unknown

Another equally valid way to use `null` is to have it
stand in for information that you do not yet know.

If you have a program ask someone for their name,
between the time you start the program and you get
a response, their name is unknown to you.

```java,no_run
String firstName = null;

// Some lines of code

firstName = askForName();
```

This is subtly different than delayed assignment. Between when
you don't know the information and when you learn it you are actually allowed
to use a variable initialized to `null`.

The difference between this kind of situation and a "known absence" is also subtle.
In this situation you do not know what a value would be. In the other you know that there
is no value to get.
