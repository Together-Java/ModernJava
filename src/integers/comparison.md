# Comparison

In addition to comparing for equality with `==`, `int`s can be compared to see if one is bigger than another using
`>`, `<`, `>=`, and `<=`.

`>` will evaluate to true if the number on the left is greater than the one on the right.

```java
boolean willBeTrue = 5 > 2;
boolean willBeFalse = 2 > 5;
```

`<` will evaluate to true if the number on the right is greater than the one on the left.

```java
boolean willBeFalse = 5 < 2;
boolean willBeTrue = 2 < 5;
```

If you went to public school like I did, you should be used to imagining that the `>` was the jaw of a shark.
Whatever direction the Jaws are facing, thats the one that would need to be bigger for the statement to be true.[^sharks]

```java
// true if the shark is facing the bigger number
// false otherwise.
boolean result = 9 🦈 5;
```

`>=` behaves the same as `>` except `>=` will evaluate to `true` if the numbers are identical, `>` will not.

```java
boolean willBeTrue = 5 >= 5;
boolean willBeFalse = 5 > 5;
```

`<=` has the same relationship to `<` as `>=` does to `>`.

```java
boolean willBeTrue = 5 <= 5;
boolean willBeFalse = 5 < 5;
```

[^sharks]: Shark attacks are far more rare than people think they are. You are not a seal. 

