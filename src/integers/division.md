# Division

You can divide any two `int`s using the `/` operator.

```java
~void main() {
int x = 8;
// y will be 4
int y = x / 2;

System.out.println(x);
System.out.println(y);
~}
```

Division with integers gives results in only the [quotient](https://www.khanacademy.org/computing/computer-science/cryptography/modarithmetic/a/the-quotient-remainder-theorem) of the result, not the remainder.

So `5 / 2` does not result in `2.5`, but instead just `2`.

```java
~void main() {
// 5 / 2 is not 2.5, but instead 2.
int x = 5 / 2;
// 13 / 3 is not 4.3333, but instead 4.
int y = 13 / 3;

System.out.println(x);
System.out.println(y);
~}
```
