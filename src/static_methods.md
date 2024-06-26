# Static Methods

If you want to be able to call a method from anywhere in your program you
can use a `static` method.

```java,no_run
class MyMath {
    static int add(int a, int b) {
        return a + b;
    }
}
```
```java
~class MyMath {
~    static int add(int a, int b) {
~        return a + b;
~    }
~}
class Main {
    void main() {
        int result = MyMath.add(1, 2);
        System.out.println(result);
    }
}
```