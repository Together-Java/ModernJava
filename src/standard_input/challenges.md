# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1

Write a program that asks a person for their name and then says 
"Hello \<their name\>" back to them.

```java,no_run
void main() {
    // 1. Call IO.readln to get their name
    // 2. Call IO.print/IO.println to say hello to them
}
```

## Challenge 2

Write a program that asks a person their age and tells them
what age they will be this time next year.

```java,no_run
void main() {
    // 1. Call IO.readln to get their age
    // 2. Interpret their age as an int
    // 3. Add one to that age
    // 2. Call IO.print/IO.println to say what age they will be next year
}
```

## Challenge 3

Write a program that asks a person for two floating point numbers and tells them
what the sum of those two numbers is

```java,no_run
void main() {
    // 1. Call IO.readln to get the first number
    // 2. Interpret that first number as a double
    // 3. Call IO.readln to get the second number
    // 4. Interpret that second number as a double
    // 5. Add the two numbers together
    // 6. Call IO.print/IO.println to say what the sum is
}
```

## Challenge 4

["Mad Libs"](https://en.wikipedia.org/wiki/Mad_Libs) are a word game where you ask people for nouns, verbs, and adjectives absent any context
and then fill them in to a template.

For example

```
I saw a <noun> today and <past tense verb>.
Unfortunately the <noun> stopped me at the <noun>.
```

Can become

```
I saw a dog today and flew.
Unfortunately the clown stopped me at the elephant.
```

Make a program that asks a user for some nouns, verbs, etc. and produces
a Mad Lib using those words.