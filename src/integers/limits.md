# Limits

Unlike in math, where numbers can be arbitrarily big or small, a Java `int`
is "fixed width."

Say you had a piece of paper that was only big enough to write two numbers on.

The only numbers you could write in a [base ten system](https://www.khanacademy.org/math/algebra-home/alg-intro-to-algebra/algebra-alternate-number-bases/v/number-systems-introduction) would be those from 0 to 99. You could not write 100 or anything larger.

A Java `int` is similar except instead of only being able to write 0 to 99 on a piece of paper, a variable that has
the type `int` can represent numbers from -2<sup>31</sup> to 2<sup>31</sup> - 1.


If you try to directly write out a number that is outside of that range, Java will not let you.

```java
// This will not run
int tooBig = 999999999999;
```

If you do math that should produce a larger number than is representable, the value will "loop around."

```java
// This is the value of 2^31 - 1
int atLimit = 2147483647;
// The value will "loop around" to -2^31
int beyondLimit = atLimit + 1;
// This will output -2147483648
System.out.println(beyondLimit);
```

There are other types which can represent a larger range of integers, as well as types
which do not have any limits, but for now `int` is the only one you will need.
