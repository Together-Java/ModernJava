# `if and else` statements


These are statements that check if something is `true` or `false`.


Here is what's avaliable:
- `if` - the classic "if" statement.
- `else` - "else" statement to check if the same condition is false.
- `else if` - mix of "if" and "else", runs some other code if an "if" statement returns false.


```java
boolean youtubeIsAmazing = false;
boolean badVibesAreGood = false;
if (youtubeIsAmazing) { // first statement to run
    System.out.println("Youtube was always amazing!");
} else if (badVibesAreGood) { // this runs if "youtubeIsAmazing" is false.
    System.out.println("Bad vibes make you strong!");
} else { // This runs if both "youtubeIsAmazing" and "badVibesAreGood" are false. (this check succeeds)
    System.out.println("Nothing is good enough.");
}
```


You can have multiple `if` and `else if` statements, but not multiple `else` statements

```
boolean goodVibesAreBad = false;
boolean programmingIsGood = true;
boolean badVibesAreGood = false;
if (goodVibesAreBad) { // first statement to run
    System.out.println("Good vibes make you weaker!");
} else if (badVibesAreGood) { // this runs if "goodVibesAreBad" is false.
    System.out.println("Bad vibes make you stronger!");
} else if (programmingIsGood) { // this runs if "goodVibesAreBad" and "badVibesAreGood" are false. (this check succeeds)
    System.out.println("Programming is cool!");
} else { // This runs if everything else is false.
    System.out.println("Nothing is good enough.");
}
```
