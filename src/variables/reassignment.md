# Reassignment

After a variable is declared and assigned an initial value, that value can be later reassigned.

```java
void main() {
    String boss = "Jaqueline";
    System.out.println(boss);
    boss = "Chelsea";
    System.out.println(boss);
}
```


Reassignments just involve the name and the new value. The type should not be redeclared.

```java
    boss = "Chelsea";
//  name   new value
```

After a variable is reassigned, the value associated with the name will reflect
the new value from that point in the program onwards.

```java
void main() {
    String boss = "Jaqueline";
    // This will output "Jaqueline"
    System.out.println(boss);
    boss = "Chelsea";
    // But this will output "Chelsea"
    System.out.println(boss);
}
```
