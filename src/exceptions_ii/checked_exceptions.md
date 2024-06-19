# Checked Exceptions

When a part of your code might throw a "checked" exception, other
parts of your code need to account for that possibility.

```java,does_not_compile
int divide(int x, int y) {
    if (y == 0) {
        // Will not work because nothing handles the exception
        throw new Exception();
    }

    return x / y;
}
~void main() {
~    
~}
```

We call them "checked" because you need to "check" for them.

These are _generally_[^thisrule] used when you expect calling code to be able to do something intelligent to recover if the exception is thrown.

[^thisrule]: This rule is merely a suggestion and people's definitions of "something intelligent" and "recover" vary wildly. Expect some things to throw checked exceptions and others to not and just know that you need to check for the checked ones.
