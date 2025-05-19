# Character

The type to use for a `char` that might be null is `Character`.

```java
~void main() {
Character c = null;
IO.println(c);
c = '%';
IO.println(c);
~}
```

Unlike a `char[]`, a `Character[]` will not be have its contents
shown when printed.

```java
~void main() {
char[] c1 = new char[] { 'a', 'b', 'c' };
IO.println(c1);

Character[] c2 = new Character[] { 'a', 'b', 'c' };
IO.println(c2);
~}
```