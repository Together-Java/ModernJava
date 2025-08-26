# Loops III


<img src="/loops_iii/header.png" height="200px"/>

Counting indexes of elements is, while effective, a tad
exhausting to do every time you want to loop through something.

```java
~void main() {
String[] shirts = new String[] {
    "T-Shirt",
    "Polo Shirt",
    "Dress Shirt"
};

for (int i = 0; i < shirts.length; i++) {
    String shirt = shirts[i];

    IO.println(shirt);
}
~}
```

This is where "for-each" loops come in.

```java
~void main() {
String[] shirts = new String[] {
    "T-Shirt",
    "Polo Shirt",
    "Dress Shirt"
};

for (String shirt : shirts) {
    IO.println(shirt);
}
~}
```
