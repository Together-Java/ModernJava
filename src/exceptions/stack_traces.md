# Stack Traces

When you get an exception, it will contain what is known as a "stack trace."

If a method `a` calls a method `b` which in turn calls a method `c`, that chain of
calls forms a "stack." 

If the method at the bottom, `c`, throws an exception that exception will contain
information about that entire "call stack."

```java,panics
void c() {
    throw new RuntimeException();
}

void b() {
    c();
}

void a() {
    b();
}

void main() {
    a();
}
```

```text,no_run
Exception in thread "main" java.lang.RuntimeException
	at Main.c(Main.java:2)
	at Main.b(Main.java:6)
	at Main.a(Main.java:10)
	at Main.main(Main.java:14)
```

This makes exceptions somewhat offensive to the eyes, but is extremely useful if something goes
wrong in a real program. You can see exactly what method had an issue and figure out where it was
called from.

Since figuring out what went wrong is a detective game, every clue helps.