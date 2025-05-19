# Null as Absence

One way to use `null` is to have it be a stand in for when there is
an "absence" of a value.

Consider [Cher](https://en.wikipedia.org/wiki/Cher). Unlike most people,
Cher does not have a last name.

`null` is an appropriate value to use when there is such an absense.

```java
~void main() {
String firstName = "Cher";
String lastName = null;

IO.println(firstName);
IO.println(lastName);
~}
```
