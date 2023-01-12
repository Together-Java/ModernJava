## Strings
Normally to check if something is equal to something, this code would be used:
```java
int one = 1;
int anotherOne = 1
if (one == anotherOne) {
    ...
}
```

but for strings, it's an entirely different story, as we use `.equals` (inherited from `Object`) instead of `==`
```java
if (stringVariable.equals("anotherString")) {
    ...
}
```

Why? because for **primitive types** (such as `int`, `float`, etc), `==` compares **values**, although **for Objects** (such as `String` and `User-Defined Classes`) and Arrays, `==` compares **references**.

So when you use `stringValue == anotherStringValue`, you're really just checking if `stringValue` is stored in the same place as `anotherStringValue` in memory

Hence, `stringValue.equals(anotherStringValue);` is used to check if `stringValue`'s value equals the value of `anotherStringValue`.
