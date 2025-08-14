# Integers

If you expect someone to type an integer value you can turn the `String`
you get from `IO.readln` into an `int` using `Integer.parseInt`.

```java,do_not_run
void main() {
    String ageString = IO.readln("How old are you? ");
    int age = Integer.parseInt(ageString);
    IO.println("You are " + age + " years old!");
}
```

So long as they type something which can be interpreted as an `int` (like `123`) 
you will get a value for the `int` variable. Otherwise
the program will crash.