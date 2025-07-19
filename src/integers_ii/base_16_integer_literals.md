# Base 16 Integer Literals

In polite society we use a base 10 number system[^everything]. This means
we start counting at `0` and go up by one until we reach `9`. 

`0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`

Then when we go up one more we put a `1` at the front and "wrap around."

`10`, `11`, `12`, etc.

In a base 16 number system, sometimes called "hexadecimal", you keep going a little
bit more before wrapping around.

`0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`, `A`, `B`, `C`, `D`, `E`, `F`, `10`, `11`, ..., `A5`, ..., `5F`, ... etc.

To write an integer literal in Java which contains a hexadecimal number you write `0x` before the number.

```java
~void main() {
int sixteen = 0x10;
IO.println(sixteen);

int twoHundredFiftyFive = 0xFF;
IO.println(twoHundredFiftyFive);
~}
```

Hexadecimal numbers like this are very common when you are writing code that
deals with colors in RGB - Red, Green, Blue - format. `0xFFFFFF` is white, `0xFF0000` is red, `0xCCCCFF` is periwinkle, etc.




[^everything]: Okay to be real with you, every number system is a base 10 system.
Even if what you call "10" is what we would call "sixteen", you always wrap around your base when you write "10." If that doesn't make sense it doesn't matter, but it's fascinating to me.