# Length

The number of elements which comprise an array can be accessed by using `.length`.[^unlike_string]

```java
~void main() {
String[] veggies = { "brussels", "cabbage", "carrots" };
int numberOfElements = veggies.length;

// veggies is 3 elements long
System.out.println(
    "veggies is " + numberOfElements + " characters long"
);
~}
```

[^unlike_string]: Unlike with a `String`, you do not write `()` after `.length`.
