# Propagating Exceptions

Say we started out with code like this.

```java
void dream() {
    System.out.println("Shin Godzilla's Jaw unhinging like a snake...")
}

void sleep() {
    dream();
}

void main() {
    sleep();
}
```

If a function is declared to throw an exception, that exception will have to "propagate" - meaning spread - to all calling functions.

```java
void dream() throws Exception {
    throw new Exception("Something went wrong")
}

void sleep() throws Exception {
    dream();
}

void main() throws Exception {
    sleep();
}
```

`dream` declares that it might throw `Exception` so `sleep` must declare that it might throw `Exception`. Because `sleep` might throw `Exception` now `main` might throw `Exception`.

