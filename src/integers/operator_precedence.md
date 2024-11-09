# Operator Precedence

Just like boolean operators, `+`, `-`, `*`, `/`, and `%` have a defined precedence order.

The order of operations is the same as mathematics. Multiplication and division happen before
addition and subtraction, with the modulo operator being a sort of "funky division."
Parentheses can be used to control this order.

None of this should be a surprise if you learned [PEMDAS](https://www.khanacademy.org/math/cc-seventh-grade-math/cc-7th-negative-numbers-multiply-and-divide/cc-7th-order-of-operations/v/introduction-to-order-of-operations) in school.

```java
~void main() {
// Following the order of operations:
// 2 * 3 + 3 * 9 / 2 - 2

// 2 * 3 happens first
// 6 + 3 * 9 / 2 - 2

// 3 * 9 happens next
// 6 + 27 / 2 - 2

// 27 / 2 happens next
// because of integer division, that gives 13
// 6 + 13 - 2

// 6 + 13 comes next
// 19 - 2

// and the final result is 17;
int result = 2 * 3 + 3 * 9 / 2 - 2;
System.out.println(result);
~}
```

The `==`, `!=`, `>`, `<`, `>=`, and `<=` operators play a part here too[^theyalldo]. They all have a lower precedence order than all the math operators, so you can
put them in the middle of any two math expressions.

```java
~void main() {
// The == check happens last.
boolean areThingsSame = 3 * (4 - 1 + 3) * 4 == 5 * 3 + 1 * 3 * 9;
System.out.println(areThingsSame);
~}
```

[^theyalldo]: Every operator in the language has a defined order of operations with respect to all of the others. I am just showing them to you as they become relevant.
