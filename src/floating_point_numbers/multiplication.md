# Multiplication

You can multiply any two `double`s using the `*` operator.

```java
~void main() {
double x = 3;
// y will be 27
double y = x * 9;
// z will be 13.5
double z = y * 0.5;

System.out.println(x);
System.out.println(y);
System.out.println(z);
~}
```

Just like with addition and subtraction, it is fine to use both integers and integer literals when doing
multiplication on doubles. So long as any number being used is a `double` the overall result will be a double.

```java
~void main() {
// a will be 3.0
double a = 1.5 * 2;
System.out.println(a);
~}
```
