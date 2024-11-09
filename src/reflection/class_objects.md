# Class Objects

You can get an object representing a class in one of a few ways.

The first is to write the name of the class followed by `.class`.
This works if you know exactly the class you want to reflect on.

While this looks like accessing a field, it is technically its own
special thing.

```java
class Main {
    void main() {
        Class<String> stringClass = String.class;
        System.out.println(stringClass);
    }
}
```

Another is to call the `getClass` method on an object. This
is a method available on `java.lang.Object` and so will work for
anything.

This is what you will use if you don't know up front exactly what
type of thing you will be reflecting over.

```java
class Main {
    void main() {
        String s = "Hello";
        Class<?> stringClass = s.getClass();
        System.out.println(stringClass);
    }
}
```

These class objects have a generic parameter that can hold the class the
class object represents.[^ifconfused] When you don't know that information
up front you should use a wildcard.


[^ifconfused]: If that seems confusing and useless, you are half
right. It certainly is confusing, but it is pretty useful sometimes.
If its still beyond your ken just always write `Class<?>` and we'll
loop back to it.