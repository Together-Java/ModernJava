# Not

Booleans can also be "negated" using the "not" operator - `!`.

```java,no_run
boolean haveOreosInHouse = true;
boolean stuckToCalorieLimit = !haveOreosInHouse;
```

So in this case, I have stuck to my calorie limit if there are _not_ Oreos in the house.

| haveOreosInHouse | stuckToCalorieLimit |
| ---------------- | ------------------- |
| false            | true                |
| true             | false               |

```java,no_run
boolean isLoggedIn = false;
boolean isGuest = !isLoggedIn;
```

Now in this case, if user is _not_ logged in he is a guest.

| isLoggedIn | isGuest |
| ---------- | ------- |
| false      | true    |
| true       | false   |
