# Shorthands for Reassignment

A very common thing to do is to take the current value of a variable, perform some simple operation like addition on it, and reassign the newly
computed value back into the variable.

```java
int x = 2;
System.out.println(x);

x = x * 5 // 10
System.out.println(x);
```

As such, there is a dedicated way to do just that.

```java
int x = 1;

// This is the same as
// x = x + 2;
x += 2;

// This is the same as
// x = x * 4
x *= 4;

// This is the same as
// x = x - (x * 5)
x -= (x * 5)

// This is the same as
// x = x / 6
x /= 6;

// This is the same as
// x = x % 3
x %= 3;

// Pop quiz!
System.out.println(x);
```

Of note is that adding or subtracting exactly 1 is common enough that it
has its own special shorthand.

```java
int x = 0;
System.out.println(x);

// Same as
// x = x + 1;
// x += 1;
x++;
System.out.println(x);

// Same as
// x = x - 1;
// x -= 1;
x--;
System.out.println(x);
```