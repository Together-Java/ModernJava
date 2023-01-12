# Ternary Expressions

**What are Ternary Expressions**?

It's a way of doing an `if` and `else` in one line as an expression, the **rules of this are simple**:

```java
someCondition ? resultIfTrue : resultIfFalse;
```

This is typically used with methods OR to replace a simple if...else statement with one line each condition.

example:
```java
String whatsGreater;
if (4 > 2) { // boolean expression which is true
    whatsGreater = "4 > 2"; // one line condition of "if"
} else { // cannot run
    whatsGreater = "2 > 4"; // another one line condition of "else"
}
System.out.println(whatsGreater);
```

can be fully replaced with:
```java
String whatsGreater = 4 > 2 ? "4 > 2" : "2 > 4";
System.out.println(whatsGreater); // 4 > 2
```

Which is really nice of java to have. ~~*gotta delete all them lines*~~
