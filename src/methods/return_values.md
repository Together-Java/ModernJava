# Return Values

In addition to running some code, a method can return a value to the code that is calling it.

To do this, instead of writing `void` before a method, you should write the name of a type like `int`.
Then at the end of the method you need to write `return` followed by something which is that type.

```java
int returnsEight() {
    return 8;
}
```

When the method is called, that expression can be used on the right hand side of an `=` to get the value returned by the method.

```java
int returnsEight() {
    return 8;
}

void main() {
    int value = returnsEight();
    System.out.println(value);
}
```

The method call can also be used directly in expressions without assigning its value to a variable first.

```java
String returnsName() {
    return "Mariah";
}

void main() {
    System.out.println(returnsName() + " is my name");
}
```
