# Performance Solutions

If the problem with the simple implementation is that we make too many copies,
the solution is to make fewer copies.

The easiest way to do this is to "over-allocate." Make our internal array bigger than
we actually need it to be. That way most of the time when you call `.add` it will be
fast.

We can't - or at least shouldn't - over allocate right away. If every growable array secretly has enough room for millions of elements that would be silly. Better to over-allocate as we go.

Exactly how much we should make the internal array bigger than we need is more art than science. People have found that doubling the size each time is a pretty good tradeoff[^important].

[^important]: This data structure is crazy important. Maybe the most common one used in the world. Java has it built-in and we'll get to that later. 