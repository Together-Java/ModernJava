# Niche Numerics

<img src="/niche_numerics/header.png" height="200px"/>

For a surprisingly wide range of programs `int` and `double`
(along with their boxed counterparts `Integer` and `Double`)
are the only numeric types you will need.

Every now and then, however, you will want something more exotic[^wording].

```java
~void main() {
byte b = 123;

IO.println(b);
~}
```

[^wording]: The reason I am calling these "exotic" and "niche" has nothing to do with how
useful they are. If you want a `byte` then a `byte` is what you want. Its just that most
of the time (in my experience) you can get by with a little help from your `int`s.