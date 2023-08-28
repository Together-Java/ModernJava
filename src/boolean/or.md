# Or

Another way booleans can be combined is by using the "or" operator - `||`.

```java
boolean dogLooksNice = true;
boolean personLooksNice = false;
boolean willAskToPetDog = dogLooksNice || personLooksNice;
```

So in this case, I will ask to pet someone's dog if either the the dog looks nice _or_ the person
walking the dog looks nice.

| dogLooksNice | personLooksNice | willAskToPetDog |
| ------------ | --------------- | --------------- |
| true         | true            | true            |
| true         | false           | true            |
| false        | true            | true            |
| false        | false           | false           |

## Exclusive vs. Inclusive

It is important too note that this is not an "exclusive" OR.

An exclusive OR would be something like
a child being allowed to have ice cream _or_ a cookie, but not both.

The `||` operator is an "inclusive" OR, meaning the child is allowed ice cream, a cookie, or both ice cream and the cookie.
