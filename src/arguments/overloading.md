# Overloading

Multiple methods can be declared that have the same name.
This is allowed so long as each method takes different types
or different numbers of arguments.

```java
void doThing(int x) {
    System.out.println(x);
}

void doThing(String name) {
    System.out.println("Hello " + name);
}

void doThing(int x, int y) {
    System.out.println(x + y);
}
```

When you call the method, Java will know what code to run
because it knows the types of and number of arguments
you are passing.

```java
void main() {
    // Java can figure out what to do
    doThing(1);
    doThing("abc");
    doThing(1, 2);
}
```

When there are multiple methods that have the same name but take different arguments,
those methods are considered "overloads" of eachother[^overload]

[^overload]:
    "Overloading" in this context means when one word has more than
    one possible meaning depending on how it is used. Buffalo buffalo Buffalo buffalo buffalo buffalo Buffalo buffalo.
