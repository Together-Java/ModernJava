# Set Individual Elements

You can also set any of the elements of an array to have a new value.

To do this, on the left hand side of an equals sign you write the name of a variable
followed by `[`, an index, and `]`. Then on the right hand side of the equals you write
the new value.[^strings]

```java
String[] sentence = { "you", "are", "found", "guilty" };
System.out.println(sentence);

sentence[1] = "aren't";
System.out.println(sentence);
```

The index of the element to set can also come from a variable.

```java
int index = 2;
String[] response = { "and", "it", "isn't", "opposite", "day" };
System.out.println(response);

response[2] = "is";
System.out.println(response);
```

If you give a number equal to or greater than the length of the array or a number less than zero, you will get an error.

```java
String[] response = { "objection" };
// Crash
response[1] = "!";
```

```java
String[] response = { "sustained" };
// Crash
response[-1] = "not";
```

[^strings]: You cannot change the contents of a `String` like you would an array. This is one of the biggest differences between a `String` and a `char[]`.
