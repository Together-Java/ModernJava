# Regular Expressions 🚧

<img src="/regular_expressions/header.png" height="200px"/>

Phone numbers in the US mostly look like `123-456-7890`. Three numbers,
a dash, three numbers, a dash, then four numbers.[^simple]

Writing the code to check if a `String` matches this pattern is tricky.

```java,no_run
boolean matchesPhoneNumberPattern(String s) {
    return s.length() == 12
        && Character.isDigit(s.charAt(0))
        && Character.isDigit(s.charAt(1))
        && Character.isDigit(s.charAt(2))
        && s.charAt(3) == '-'
        && Character.isDigit(s.charAt(4))
        && Character.isDigit(s.charAt(5))
        && Character.isDigit(s.charAt(6))
        && s.charAt(7) == '-'
        && Character.isDigit(s.charAt(8))
        && Character.isDigit(s.charAt(9))
        && Character.isDigit(s.charAt(10))
        && Character.isDigit(s.charAt(11))
}
```

For situations like this a useful tool is something called "regular expressions"
and the `Pattern` class.

```java,no_run
boolean matchesPhoneNumberPattern(String s) {
    return Pattern.compile("(\\d\\d\\d)-(\\d\\d\\d)-(\\d\\d\\d\\d)")
        .asMatchPredicate()
        .test(s);
}
```


[^simple]: A common, but understandable, mistake is assuming that formats
like phone numbers are actually this simple. Phone numbers and emails are always a little
bit of a nightmare to validate.