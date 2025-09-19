# For-each loops

Where a normal `for` loop is more or less a shorthand for a certain kind of `while` loop, 
a for-each loop[^enhanced] is a shorthand for the general concept of iterating over a collection
of elements.

To use a for-each loop, write `for` then in the parentheses write a variable declaration, a `:`, and the
collection of elements you are iterating over.

```
for (<VARIABLE DECLARATION> : <COLLECTION>) {
    <BODY>
}
```

```java
record Bread(String name, boolean french) {}

~class Main {
~    void main() {
Bread[] breads = { 
    new Bread("Croissant", true),
    new Bread("Baguette", true),
    new Bread("Boston Brown Bread", false)
};

for (Bread bread : breads) {
    IO.println(
        bread.name()
            + (bread.french() ? " is french" : " is not french")
        );
}
~    }
~}
```


[^enhanced]: You might see this referred to as an "enhanced for statement." [That is its name in the language spec](https://docs.oracle.com/javase/specs/jls/se25/html/jls-14.html#jls-14.14.2) but not the name most people will use.