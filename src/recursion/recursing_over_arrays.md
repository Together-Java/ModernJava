# Recurse Over an Array

To write a recursive function which acts over each element
of an array, the technique is the same as with you need to do much the same task as with regular loops,
just by having your "current index" be a parameter to the function.

```java
class Main {
    void printEachTimesEight(int[] nums, int i) {
        if (i < nums.length) {
            System.out.println(nums[i] * 8);
            printEachTimesEight(nums, i + 1);
        }
    }

    void printEachTimesEight(int[] nums) {
        printEachTimesEight(nums, 0);
    }

    void main() {
        printEachTimesEight(new int[] { 1, 2, 3 });
    }
}
```

This same general technique can be used to loop over other sorts of collections, like `ArrayList`. In that
case you would use `.get()` and `.size()` instead of `[]` and `.length`, but the concept is the same.