# Math

One of the most "obvious" usages for static methods is when doing things
that are math or math-like.

```java,no_run
class MyMath {
    static int add(int a, int b) {
        return a + b;
    }
}
```

These sorts of methods have a result computed solely from their inputs, so needing
an instance of a class to call them would be silly.

The `Math` class that comes with Java has methods that work in this way. `Math.max(a, b)`
is `static` and therefore usable everywhere you want the maximum of two numbers.[^more]

[^more]: There are way more on there. [Take a look](https://docs.oracle.com/en/java/javase/25/docs/api/java.base/java/lang/Math.html).