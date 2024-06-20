# Private Inner Classes

Both `static` and regular inner classes can be marked as `private`.

```java
class Human {
    // No other class can see this human's thoughts
    private class Thoughts {

    }

    // Nor can they see their feelings
    private static class Feelings {

    }
}
```

Within the class they are defined, a private inner class works as normal. The
difference is that code outside the class cannot make instances of them.