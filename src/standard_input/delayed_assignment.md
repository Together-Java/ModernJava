# Delayed Assignment

When you have variables declared inside of that loop cannot be seen from the outside.
This poses a problem when you are asking someone a question in a loop but want their response to be
visible later on in the program.

One strategy for this is to declare any response-holding variables outside the loop.

The problem with this is that Java isn't smart enough to know that you always initialize those variables.

```java,no_run,does_not_compile
void main() {
    String name;
    while (true) {
        String name = IO.readln("What is your name? ");
        if (name.isBlank()) {
            IO.println("Name cannot be blank!");
            continue;
        }

        break;
    }

    IO.println("Hello " + name);
}
```

To get around this you can either give an explicit default value.

```java,no_run
void main() {
    String name = null;
    while (true) {
        String name = IO.readln("What is your name? ");
        if (name.isBlank()) {
            IO.println("Name cannot be blank!");
            continue;
        }

        break;
    }

    IO.println("Hello " + name);
}
```

Or you can use the `do` version of a while loop. 
In this context our old friend delayed assignment becomes an option again. This is because Java *is* smart enough
to see that the code in the loop will run at least once.

```java,no_run
void main() {
    String name;
    do {
        String name = IO.readln("What is your name? ");
        if (name.isBlank()) {
            IO.println("Name cannot be blank!");
            continue;
        }

        break;
    } while (true);

    IO.println("Hello " + name);
}
```