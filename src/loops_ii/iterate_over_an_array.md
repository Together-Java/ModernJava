# Iterate over an Array

In the same way you can use a `for` loop to go through each character of a `String`,
you can use it to go through each element in an array.

```java
~void main() {
int[] numbers = { 4, 1, 6, 9 };

for (int index = 0; index < numbers.length; index++) {
    System.out.println(numbers[index]);
}
~}
```

The only difference from `String`s is that instead of `.length()` and `.charAt(...)`, you use `.length` and `[]`.
