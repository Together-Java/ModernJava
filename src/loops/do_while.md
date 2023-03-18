# Do

One variation on a while loop is a "do-while loop."

```java
int x = 0;
do {
    System.out.println(x);
    x++
} while(x < 5);
```

You write `do`, some code inside of `{` and `}`, and then `while`, a condition inside of
`(` and `)`, and finally a semicolon.

```java
do {
    <CODE HERE>
} while (CONDITION);
```

In most situations it works exactly the same as a regular while loop. The only difference
is that the first time the loop is reached the condition for the loop is not checked.

```java
int x = 0;
do {
    System.out.println("this will run");
} while (x != 0)

while (x != 0) {
    System.out.println("this will not run");
}
```

One way to remember the difference is that in a "do-while loop" you always "do the thing"
at least once.