# And

One way multiple booleans can be combined is by using the "and" operator - `&&`.

```java
boolean funToBeAround = true;
boolean believesInFundamentalHumanRights = true;
boolean willAskOnDate = funToBeAround && believesInFundamentalHumanRights;
```

So in this case, I will ask someone on a date if they are fun to be around _and_
they wholeheartedly believe in the assertions made in the [Universal Declaration of Human Rights](https://www.un.org/en/about-us/universal-declaration-of-human-rights).

| funToBeAround | believesInFundamentalHumanRights | willAskOnDate |
|---------------|----------------------------------|---------------|
| true          | true                             | true          |
| true          | false                            | false         |
| false         | true                             | false         |
| false         | false                            | false         |
