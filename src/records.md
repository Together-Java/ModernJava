# Records

If you have a class whose only purpose is to ferry data around,
you can instead use a `record`.

```java
record Person(String name, int age) {}
```