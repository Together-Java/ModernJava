# Difference between Initializer and Literal

The reason `{ 1, 2, 3 }` is called an "array initializer" and not
an "array literal" is somewhat subtle.

When you have a literal, like a `String` literal, you can assign that to a variable and
then use that `String` afterwards.

```java
String name = "Alana";
// l
System.out.println(name.charAt(1));
```

But you can also perform those operations using the literal itself, without an intermediate variable.

```java
// l
System.out.println("Alana".charAt(1));
```

Array initializers work in the case where you first assign them to a variable before using
the array.

```java
char[] name = { 'A', 'm', 'a', 'n', 'd', 'a' };
// m
System.out.println(name[1]);
```

But they do not work to perform operations on directly.

```java
// Will not run
System.out.println({ 'A', 'm', 'a', 'n', 'd', 'a' }[1]);
```