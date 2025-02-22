# @Override

The `@Override` you can put on methods to have Java check that you are properly overriding them
is an annotation.

There's not much else to say besides "hey, thats what that was!" but I think its
worth noting.

```java
interface Num {
    boolean odd();

    boolean even();
}

class IntNum implements Num {
    final int x;

    IntNum(int x) {
        this.x = x;
    }

    @Override // This is an annotation?
    public boolean odd() {
        return x % 2 != 0;
    }

    @Override // Always has been.
    public boolean even() {
        return !odd();
    }
}
```