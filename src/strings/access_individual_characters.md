# Access Individual Characters

Given a `String`, you can access the individual characters which
comprise it by using `.charAt`.

The first character can be accessed by putting `0` in the parentheses.
The second by using `1`, and so on.

```java
~void main() {
String spy = "loid";

char l = spy.charAt(0);
IO.println(l);

char o = spy.charAt(1);
IO.println(o);

char i = spy.charAt(2);
IO.println(i);

char d = spy.charAt(3);
IO.println(d);
~}
```

We call this number the "index" of the character.[^otherds]

The index of the character to access can come from a variable.

```java
~void main() {
String assassin = "yor";
int indexOfR = 2;

char r = assassin.charAt(indexOfR);
IO.println(r);
~}
```

If you give a number equal to or greater than the length of the `String` or a number less than zero,
you will get an error.

```java,panics
~void main() {
String student = "anya";
// Crash!
student.charAt(999);
~}
```

```java,panics
~void main() {
String dog = "bond";
// Crash!
dog.charAt(-1);
~}
```

[^otherds]: There will be more things which have their individual elements accessible by indexes. They will all generally start from 0 for the first element but there are rare exceptions.
