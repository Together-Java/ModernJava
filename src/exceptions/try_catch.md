# try/catch


If you know that some code might fail, and you have an idea of what to do if it does,
you can prevent an exception from crashing your program by `catch`-ing it.

To do this, you write `try` and put the code that might fail inside of `{` and `}`.

```java,no_run,panics
try {
    mightFail();
}
```

Then you write `catch` and in parentheses the kind of exception you want to handle as well as a variable name.[^needvar]

```java,no_run
try {
    mightFail();
} catch (RuntimeException e) {

}
```

And inside the catch block you can write code to run when such an exception occurs.

```java,panics
void doThing(int x) {
    if (x == 0) {
        throw new RuntimeException("Cannot do something zero times");
    }
}

void main() {
    int x = 0;
    try {
        doThing(x);
    } catch (RuntimeException e) {
        System.out.println("Something went wrong doing a thing.");
    }
}
```

Just as you cannot have an `else` without an `if`, you cannot have a `catch` without a `try`.

```java,does_not_compile
void main() {
    catch (RuntimeException e) {
        System.out.println("Hello");
    }
}
```

Nor can you have a `try` without a `catch`.[^trywithresources]

```java,does_not_compile
void main() {
    try {
        System.out.println("Hello");
    }
}
```

[^needvar]: Generally you will just use `e` for this. Even if you don't call any instance methods on the exception, you still need to give a name for it.

[^trywithresources]: Technically you can have a `try` without a `catch`, but only when using another feature of
Java you haven't been shown yet. It will make sense when the time comes.
