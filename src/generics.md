# Generics

Certain types of classes, like growable arrays, are simply holders of data.

That is, almost none of how they work has to change to
store different kinds of data.

Generics help us make these generically useful containers.

```java
class Box<T> {
    T value;
}
```