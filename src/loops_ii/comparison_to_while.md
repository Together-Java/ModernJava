# Comparison to while

If you were to compare the code needed to loop over an array using a `for` loop
and the code needed with a `while` loop, there might not seem like much of a difference.

```java
double[] numbers = { 4.4, 1.1, 4.1, 4.7 };

for (int index = 0; index < numbers.length; index++) {
    System.out.println(numbers[index]);
}

int index = 0;
while (index < numbers.length) {
    System.out.println(numbers[index]);
    index++;
}
```

This is doubly true when we are looking at toy examples where the only thing done
with the element is `System.out.println`.

The biggest benefit to a `for` is subtle. With a `while` based loop, the initializer and boolean expression
can potentially be many lines from the statement which updates the variable.

```java
int index = 0;
while (index < numbers.length) {
    /*
    Can


    potentially

    have

    arbitrary

    code

    you want to run

    a bunch

    of times
    */

    index++;
}
```

Us humans, with our tiny monkey brains, can get very lost when things that are related to eachother are separated
by long distances.

In this dimension, for loops are superior. All the bits of code that "control the loop" can be right at the top.

```java
for (int index = 0; index < numbers.length; index++) {
    /*
    Can


    potentially

    have

    arbitrary

    code

    you want to run

    a bunch

    of times
    */
}
```