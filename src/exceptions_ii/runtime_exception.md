# RuntimeException

`RuntimeException` is an unchecked exception.[^naming]

If you want a unchecked exception and do not know of a better one, `RuntimeException` will do.

```java,panics
void main() {
    throw new RuntimeException("Crash!");
}
```

[^naming]: You may be wondering why the names "`Exception`" and "`RuntimeException`" instead of the
probably easier to understand "`CheckedException`" and "`UncheckedException`." Java was made by humans
and initially - as I understand it - "normal" exceptions were expected to be checked. It was only
exceptions that came from "The Java Runtime" that would be unchecked. So that is where the name "`RuntimeException`" comes from. It just very quickly became a choice that was too late to change
without breaking all the Java code in the world.