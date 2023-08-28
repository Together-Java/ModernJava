# Challenges

Early on, most students tend to have a lot of trouble with loops.
Its also what is quizzed on in a lot of standardized tests.

Because of that there will be a lot of challenges in this section for you
to practice. Try to at least do the first ten or so to make sure you have
the concept down, but the more the better.

It might take awhile before you feel truly comfortable with this. That is normal.

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1

Write code that outputs every number from `1` to `10`.

~IF toplevel_anonymous_class

```java
void main() {
    <CODE HERE>
}
```

~ELSE

```java
public class Main {
    public static void main(String[] args) {
        <CODE HERE>
    }
}
```

~ENDIF

## Challenge 2

What will this program output when run? Write down your guess and then try running it.

~IF toplevel_anonymous_class

```java
void main() {
    int x = 0;
    while (x < 10) {
        System.out.println(x);
        x++;
    }
}
```

~ELSE

```java
public class Main {
    public static void main(String[] args) {
        int x = 0;
        while (x < 10) {
            System.out.println(x);
            x++;
        }
    }
}
```

~ENDIF

## Challenge 3

What will this program output when run? Write down your guess and then try running it.

~IF toplevel_anonymous_class

```java
void main() {
    int x = 0;
    while (x <= 10) {
        System.out.println(x);
        x++;
    }
}
```

~ELSE

```java
public class Main {
    public static void main(String[] args) {
        int x = 0;
        while (x <= 10) {
            System.out.println(x);
            x++;
        }
    }
}
```

~ENDIF

## Challenge 4

What will this program output when run? Write down your guess and then try running it.

~IF toplevel_anonymous_class

```java
void main() {
    int x = 0;
    while (x < 10) {
        if (x % 3 == 0) {
            break;
        }
        System.out.println(x);
        x++;
    }
}
```

~ELSE

```java
public class Main {
    public static void main(String[] args) {
        int x = 0;
        while (x < 10) {
            if (x % 3 == 0) {
                break;
            }
            System.out.println(x);
            x++;
        }
    }
}
```

~ENDIF

## Challenge 5

What will this program output when run? Write down your guess and then try running it.

~IF toplevel_anonymous_class

```java
void main() {
    int x = 0;
    while (x < 10) {
        if (x % 3 == 0) {
            continue;
        }
        System.out.println(x);
        x++;
    }
}
```

~ELSE

```java
public class Main {

    public static void main(String[] args) {
        int x = 0;
        while (x < 10) {
            if (x % 3 == 0) {
                continue;
            }
            System.out.println(x);
            x++;
        }
    }
}
```

~ENDIF

## Challenge 6

What will this program output when run? Write down your guess and then try running it.

~IF toplevel_anonymous_class

```java
void main() {
    int x = 1;
    while (x < 10) {
        int y = 2;
        while (y < 5) {
            System.out.println(x * y);
            y++;
        }

        x++;
    }
}
```

~ELSE

```java
public class Main {
    public static void main(String[] args) {
        int x = 1;
        while (x < 10) {
            int y = 2;
            while (y < 5) {
                System.out.println(x * y);
                y++;
            }

            x++;
        }
    }
}
```

~ENDIF

## Challenge 7

What will this program output when run? Write down your guess and then try running it.

~IF toplevel_anonymous_class

```java
void main() {
    <CODE HERE>
}
```

~ELSE

```java
public class Main {
    public static void main(String[] args) {
        int x = 0;
        String scream = "a";
        while (!scream.equals("aaaaaaaa")) {
            scream = scream + "a";
            System.out.println(x);
            System.out.println(scream);
        }
    }
}
```

~ENDIF

## Challenge 8

Write code that will output each character of `name` on its own line.

So for if `name` is equal to `"Bridget"`, I would expect the following as output.

```text
B
r
i
d
g
e
t
```

~IF toplevel_anonymous_class

```java
void main() {
    <CODE HERE>
}
```

~ELSE

```java
public class Main {
    public static void main(String[] args) {
        // Change this value to test your code.
        String name = "Bridget";

        // <CODE HERE>
    }
}
```

~ENDIF

## Challenge 9

Write code that will output each character of `name` on its own line, starting with the last
character and going backwards.

So for if `name` is equal to `"Samantha"`, I would expect the following as output.

```text
a
h
t
n
a
m
a
S
```

~IF toplevel_anonymous_class

```java
void main() {
    // Change this value to test your code.
    String name = "Samantha";

    // <CODE HERE>
}
```

~ELSE

```java
public class Main {
    public static void main(String[] args) {
        // Change this value to test your code.
        String name = "Samantha";

        // <CODE HERE>
    }
}
```

~ENDIF

## Challenge 10

Write code that will take a number and if it is divisible by two, divides it by two.
If it is not, multiplies it by three and adds one.

Keep doing this until the number equals one. Output it each time.

If the initial number is `6` you should have this as output.

```text
6
3
10
5
16
8
4
2
1
```

If the initial number is `15` you should have this as output.

```text
15
46
23
70
35
106
53
160
80
40
20
10
5
16
4
2
1
```

~IF toplevel_anonymous_class

```java
void main() {
    // Change this value to test your code.
    int n = 15;

    // <CODE HERE>
}
```

~ELSE

```java
public class Main {
    public static void main(String[] args) {
        // Change this value to test your code.
        int n = 15;

        // <CODE HERE>
    }
}
```

~ENDIF

## Challenge 11

Write code that outputs every third number from `37` to `160`.

~IF toplevel_anonymous_class

```java
void main() {
    <CODE HERE>
}
```

~ELSE

```java
public class Main {
    public static void main(String[] args) {
        <CODE HERE>
    }
}
```

~ENDIF

## Challenge 12

Write code that outputs the number of vowels in `name`. Treat `y` as a vowel.

Treat the characters `a`, `A`, `e`, `E`, `i`, `I`, `o`, `O`, `u`, `U`, `y`, and `Y` as vowels.

~IF toplevel_anonymous_class

```java
void main() {
    // Change this value to test your code.
    String name = "Damian";

    // <CODE HERE>
}
```

~ELSE

```java
public class Main {
    public static void main(String[] args) {
        // Change this value to test your code.
        String name = "Damian";

        // <CODE HERE>
    }
}
```

~ENDIF

## Challenge 13

Write code that outputs `{name} is mostly vowels` if the number of vowels in `name` is greater
than the number of consonants. and `{name} is mostly consonants` if the opposite is true.
Output `{name} has an equal number of vowels and consonants` if the count of both is the
same.

Make sure to not treat non-alphabetic characters like `!` and `?` as consonants.

~IF toplevel_anonymous_class

```java
void main() {
    // Change this value to test your code.
    String name = "Messi";

    // <CODE HERE>
}
```

~ELSE

```java
public class Main {
    public static void main(String[] args) {
        // Change this value to test your code.
        String name = "Messi";

        // <CODE HERE>
    }
}
```

~ENDIF

## Challenge 14

Rewrite the following code to not have the `shouldBreak` variable
and instead to use a labeled break.

~IF toplevel_anonymous_class

```java
void main() {
    // Don't think too hard about what these numbers mean.
    int x = 3;
    int y = 0;

    boolean shouldBreak = false;
    while (shouldBreak && x < 100) {
        while (y < 100) {
            System.out.println("x is " + x);
            System.out.println("y is " + y);
            x = x * y;
            if (x == 0) {
                shouldBreak = true;
                break;
            }
            y++;
        }
    }

    System.out.println("Done");
}
```

~ELSE

```java
public class Main {
    public static void main(String[] args) {
        // Don't think too hard about what these numbers mean.
        int x = 3;
        int y = 0;

        boolean shouldBreak = false;
        while (shouldBreak && x < 100) {
            while (y < 100) {
                System.out.println("x is " + x);
                System.out.println("y is " + y);
                x = x * y;
                if (x == 0) {
                    shouldBreak = true;
                    break;
                }
                y++;
            }
        }

        System.out.println("Done");
    }
}
```

~ENDIF
