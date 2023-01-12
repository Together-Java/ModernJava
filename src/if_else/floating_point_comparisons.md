# `Floating Point Number` comparisons.
If you don't know the conditions in java, we'd suggest you to check out [this](./if_else/if_statement.md)

Here's an example of a floating point number comparison between a number and another.
**Example:**
```java
double number = 56.78;
double anotherNumber = 56.79; // notice the .01 difference
if (number < anotherNumber) { // true
    System.out.println("56.79 > 56.78");
} else { // not running because it's impossible for 56.78 to be greater than 56.79
    System.out.println("56.78 > 56.79");
}
```
 
