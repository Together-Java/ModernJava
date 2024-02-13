# Local Variables

Mechanically, the next thing to cover is "variables".


```java
void main() {
    String boss = "Jaqueline";
    System.out.println(boss);
}
```

A variable declaration has three components - the "type", the "name", and the "initial value".

```java,no_run
```java,no_run
     String boss = "Jaqueline";
//   type   name   initial value
```

In this case, we are declaring a variable called "boss" and assigning it the initial value
of `"Jaqueline"`. Its "type" is "String", which I'll explain in more detail a bit ahead.

After you declare a variable and assign it a value, the "name" refers to the value on the right
hand side and you can use that name instead of the value.

```java
~void main() {
// Does the same thing as System.out.println("Jaqueline");
String boss = "Jaqueline";
System.out.println(boss);
~}
```
