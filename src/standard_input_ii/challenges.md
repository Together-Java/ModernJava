# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1

Write a program that asks which Twilight character Bella should have ended up with.

It should keep asking this question until the user types the magic words "i do not care" 

```java,no_run
void main() {
    // CODE HERE
}
```

## Challenge 2

Update the program above to also accept "I DO NOT CARE", "I Do Not Care", and
any other mix of capital and lower-case letters


## Challenge 3

Write a method called `askForBirthday` that asks for the year, month, and day that someone was born.
This method should return all three pieces of information with a `Birthday` class.

```java,no_run
class Birthday {
    // CODE HERE
}

Birthday askForBirthday() {
    // CODE ALSO HERE
}

void main() {
    Birthday b = askForBirthday();
    IO.println(b.year + "-" + b.month + "-" + b.day)
}
```

## Challenge 4

Update the program above to reprompt the user if they enter any nonsensical information
for the year, month, or day. This includes negative numbers for the year, month, or day.

## Challenge 5

Update the birthday program to represent the month with an enum named `Month`.

Accept both the name of the month with any capitalization and the number of the month (starting with `1` for January) as valid ways to specify the month.

Make sure to still reprompt on unexpected inputs.

```java,no_run
enum Month {
    JANUARY,
    FEBRUARY,
    MARCH,
    APRIL,
    MAY,
    JUNE,
    JULY,
    AUGUST,
    SEPTEMBER,
    NOVEMBER,
    DECEMBER
}

class Birthday {
    // CODE HERE
}

Birthday askForBirthday() {
    // CODE ALSO HERE
}

void main() {
    Birthday b = askForBirthday();
    IO.println(b.year + "-" + b.month + "-" + b.day)
}
```
