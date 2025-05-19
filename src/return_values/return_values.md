# Return Values

You can use a method call on the right hand side of an `=` to get the value returned by the method.

```java
int returnsEight() {
    return 8;
}

void main() {
    int value = returnsEight();
    IO.println(value);
}
```

The method call can also be used directly in expressions without assigning the value to a variable first.

```java
String returnsName() {
    return "Mariah";
}

void main() {
    IO.println(returnsName() + " is my name");
}
```
