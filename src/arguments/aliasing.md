# Aliasing

Because arguments work like variables, if you pass something
like an array as an argument the array referenced by the argument will be the exact same as the array referenced by the variable given to the method.

```java
void incrementFirst(int[] numbers) {
    numbers[0] = numbers[0] + 1;
}

void main() {
    int[] nums = new int[] { 8 };

    // The first number is 8
    System.out.println(
        "The first number is " + nums[0]
    );

    incrementFirst(nums);

    // Now it is 9
    System.out.println(
        "Now it is " + nums[0]
    );
}
```

The argument aliases the value passed to the method.
