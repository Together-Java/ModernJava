# Inferred Types

In many cases, Java is smart enough to know what the type of a variable should be
based on what it is initially assigned to.
In these cases, you can write `var` in place of the type and let java "infer" what it should
be.


```java
// Since what is to the right hand side
// of the = is in quotes, Java knows that
// it is a String.
var theDude = "Lebowski";
System.out.println(theDude);
```

You cannot use `var` with variables whose assignment is delayed.

```java
// With just the line "var theDude;",
// Java doesn't know enough to infer the type
var theDude;
theDude = "Lebowski";
System.out.println(theDude);
```

You can use `var` with `final` to make a variable whose type is inferred
and cannot be reassigned.

```java
final var theDude = "Lebowski";
System.out.println(theDude);
```

Important to note that even if Java is smart enough to automatically know the type,
you might not be yet. There is no shame in writing out the type explicitly.

```java
String theDude = "lebowski";
```