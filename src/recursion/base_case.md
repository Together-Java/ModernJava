# Base Case

The general structure of a recursive method is that
it will sometimes call itself and sometimes not.

This makes sense if you think about it. If it always called
itself, it would never stop calling itself and run forever.

We call the case where the function will not call itself 
a "base case"

```java,no_run
if (<SOMETHING>) {
    <CALL SELF>
}
else {
    // The base case
    return <VALUE>;
}
```