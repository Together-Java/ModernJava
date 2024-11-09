# equals and hashCode

In addition to `toString`, two methods that all `Object`s have defined
are `equals` and `hashCode`.

`equals` is a method that takes another object and returns a `boolean` based
on whether you would consider those objects to be equivalent.

By default, `equals` will behave identically to `==`.

```java
class Thing {}

class Main {
    void main() {
        var t1 = new Thing();
        var t2 = new Thing();

        System.out.println(t1 == t1);
        System.out.println(t1.equals(t1));

        System.out.println(t2 == t2);
        System.out.println(t2.equals(t2));


        System.out.println(t1 == t2);
        System.out.println(t1.equals(t2));
    }
}
```

Many types will have `equals` overridden to do things like return equal if
the types represent the same context, as is the case with `Integer`.

```java
class Main {
    void main() {
        Integer a = 3;
        Integer b = 3;
        Integer c = 4;

        System.out.println(a.equals(b));
        System.out.println(a.equals(c));
    }
}
```

`hashCode` is a method that tells you if things _might_ be equal. It returns an `int`.
If two objects give different hash codes then its assumed that the result of `a.equals(b)`
will be `false`. If they give the same hash code, then the result of `a.equals(b)` might
be either `true` or `false`.

Its sort-of like asking what the first letter of someone's name is. If their names start with different letters
they definitely have different names. If their names both start with `B` they _might_ both be named Bob, but maybe one is Bob and the other is Barry.

```java
class Thing {}

class Main {
    void main() {
        String a = "abc";
        String b = "abc";
        String c = "bca";

        System.out.println(a.hashCode());
        // a.equals(b) will return true, so they will have the same hash code
        System.out.println(b.hashCode());
        // a.equals(c) will return false, so they may or may not have the same hash code
        System.out.println(c.hashCode());

        Thing t1 = new Thing();
        Thing t2 = new Thing();

        // The default .equals() is the same as ==
        System.out.println(t1.hashCode());
        System.out.println(t2.hashCode());
    }
}
```
