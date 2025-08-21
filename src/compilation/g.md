# -g

There are a lot of options you can pass to `javac` to alter its behavior.
One of the ones that I find useful is `-g`. The `g` stands for "**g**enerate debug info."[^obvious]

This makes sure the generated class files have information about things like what variables were named
what. This, in turn, helps Java give better error messages

For example, if you have a program like the following:

```java
class Main {
    void main() {
        String nocturne = null;
        IO.println(nocturne.length());
    }
}
```

While in all situations it will ultimately crash with a `NullPointerException`, if
you did not compile with `-g` you might get a stack trace like the following. 
You will probably need to scroll to the right to see the relevant bit.

```text,no_run
Exception in thread "main" java.lang.NullPointerException: Cannot invoke "String.length()" because "<local1>" is null
	at Main.main(Main.java:4)
```

Whereas using `-g` will get you an exception that includes the variable name of what was `null`.

```text,no_run
Exception in thread "main" java.lang.NullPointerException: Cannot invoke "String.length()" because "nocturne" is null
	at Main.main(Main.java:4)
```

So, with rare exceptions, you should always use `-g`.  


[^obvious]: Obviously.