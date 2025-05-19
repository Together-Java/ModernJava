# Accessing Arguments

To access the command line arguments given to your program you need to change your main method.

Instead of 

```java
void main() {

}
```

Have your main method take a string array as an argument.

```java
void main(String[] args) {

}
```

This `String[]` will hold all the arguments passed.

```
java src/Main.java Duck Squirrel
```

```java
~class Main {
void main(String[] args) {
    for (int i = 0; i < args.length; i++) {
        IO.println(
            "Hello Mr. " + args[i]
        );
    }
}
~}
~// This is a little ugly
~void main() {
~    new Main().main(new String[] { "Duck", "Squirrel" });   
~}
```
