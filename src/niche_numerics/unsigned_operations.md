# Unsigned Operations

While a `byte` represents a signed value between `-128`
and `127`, its not uncommon to instead want to represent a number between `0` and `255`.
We call representations like that, where we repurpose what would be negative numbers to instead be large positive numbers, "unsigned." 

All of Java's built-in numeric types are signed, but you can use static methods
to perform operations on them that work as if they were unsigned.

```java
~void main() {
// Java sees 255 as being out of range for a byte
// so we have to cast
byte b = (byte) 255;
// And by default this will be seen as -127
System.out.println(b);
// But we can use Byte.toUnsignedInt to see it
// as 255
System.out.println(Byte.toUnsignedInt(b));
~}
```

Operations like addition with `+` don't need special unsigned versions since they work "the same" regardless of whether you ultimately choose to interpret your numbers as unsigned or signed. Other operations like division or comparisons need special logic
to work right when doing "unsigned math."

```java
~void main() {
int i = -1;
// -1 is actually 4294967295 when viewed as an unsigned int
System.out.println(Integer.toUnsignedString(i));
// So normal comparisons won't do what you want
boolean isFiveBigger = 5 > i;
System.out.println(isFiveBigger);
// You'd want to use special unsigned comparisons
isFiveBigger = Integer.compareUnsigned(5, i) > 0;
System.out.println(isFiveBigger);
~}
```

All these special unsigned operations are `static` methods on each type's corresponding
boxed equivalent class. What static methods are available varies from type to type.