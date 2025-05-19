# NullPointerException

If you try to perform an operation on a `null` reference,
such as checking the `.length()` of a `String`, your code will
crash.

```java,panics
void main() {
    String thing = null;
    // NullPointerException
    IO.println(thing.length());
}
```

When this happens the error that Java shows you will be a "`NullPointerException`".
This will look something like the following.

```text,no_run
Exception in thread "main" java.lang.NullPointerException: Cannot invoke "String.length()" because "thing" is null
	at Main.main(Main.java:4)
```

Because this is easy to make happen by mistake, it is worth familiarizing yourself with the format
of it.

This way you can laser focus on the part that says something like "`Cannot invoke "String.length()" because "thing" is null`" and know that the issue is with some variable named `thing` 
that you are trying to call `.length()` on.