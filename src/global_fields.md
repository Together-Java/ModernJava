# Global Fields

You can make field declarations outside of a class.
This makes these fields "global" to the program.

We call things global when they are available at every point
in the "world" of our program.[^wonthold]

```java
int number = 0;

void main() {
    IO.println(number);
    number++;
    IO.println(number);
}
```

[^wonthold]: This explanation is I think a correct description of what it means
to be global, but what I am showing won't really hold up as a global thing the more you learn.