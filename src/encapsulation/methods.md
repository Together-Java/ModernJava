# Methods

The simplest mechanism for encapsulating implementation details
is a method.

The `Math.sin` function that comes with Java has a definition that looks
something like this.[^liberties]

```java,no_run
double sin(double x) {
    double[] y = new double[2];
    double z = 0.0;
    int n, ix;

    // High word of x.
    ix = __HI(x);

    // |x| ~< pi/4
    ix &= EXP_SIGNIF_BITS;
    if (ix <= 0x3fe9_21fb) {
        return __kernel_sin(x, z, 0);
    } else if (ix >= EXP_BITS) {  // sin(Inf or NaN) is NaN
         return x - x;
    } else { // argument reduction needed
        n = RemPio2.__ieee754_rem_pio2(x, y);
        // ...
    }
}
```

People who write programs that depend on the `sin` function do not generally
understand how this works. I have a math minor[^notimpressive] and I certainly don't.

All they need to know to use `sin` effectively is what it does, not how it does it.
In this way `sin`, and most methods, are one way to provide encapsulation. You reduce
a potentially complicated body of code to inputs requires and outputs produced.

[^liberties]: I took some creative liberties here, roll with it.

[^notimpressive]: Laugh it up.