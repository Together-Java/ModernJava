# Set Individual Elements

You can also set any of the elements of an array to have a new value.

To do this, on the left hand side of an equals sign you write the name of a variable
followed by `[`, an index, and `]`. Then on the right hand side of the equals you write
the new value.[^strings]

```java
~void main() {
String[] sentence = { "you", "are", "found", "guilty" };
IO.println(
    sentence[0] 
        + " " 
        + sentence[1] 
        + " " 
        + sentence[2] 
        + " " 
        + sentence[3]
);

sentence[1] = "aren't";
IO.println(
    sentence[0] 
        + " " 
        + sentence[1] 
        + " " 
        + sentence[2] 
        + " " 
        + sentence[3]
);
~}
```

The index of the element to set can also come from a variable.

```java
~void main() {
int index = 2;
String[] response = { "and", "it", "isn't", "opposite", "day" };
IO.println(
    response[0] 
        + " " 
        + response[1] 
        + " " 
        + response[2] 
        + " " 
        + response[3]
        + " "
        + response[4]
);

response[index] = "is";
IO.println(
    response[0] 
        + " " 
        + response[1] 
        + " " 
        + response[2] 
        + " " 
        + response[3]
        + " "
        + response[4]
);
~}
```

If you give a number equal to or greater than the length of the array or a number less than zero, you will get an error.

```java,panics
~void main() {
String[] response = { "objection" };
// Crash
response[1] = "!";
~}
```

```java
~void main() {
String[] response = { "sustained" };
// Crash
response[-1] = "not";
~}
```

[^strings]: You cannot change the contents of a `String` like you would an array. This is one of the biggest differences between a `String` and a `char[]`.
