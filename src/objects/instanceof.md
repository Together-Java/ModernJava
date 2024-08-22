# instanceof

If you have an `Object` you can recover the actual type
of the data stored in it using `instanceof`.

```java
~void main() {
Object o = "123";

if (o instanceof String) {
    System.out.println("This object is a String!");
}
~}
```

Inside an `if` you give the name of a field or variable
whose type is `Object`. Then you write `instanceof`
followed by the type you want to see if that object
is an instance of.

You can also give a variable name after the type.
This will let you call methods from the actual type that are otherwise
unavailable when all Java knows is that you have an `Object`.

```java
~void main() {
Object o = "123";

if (o instanceof String s) {
    System.out.println(
        "Can call String methods after recovering the type: " + s.charAt(0)
    );
}
~}
```
