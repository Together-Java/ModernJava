# Importance

So why is this person's take important for you to know about?

The reason is that the core concept - that
every observable property will be depended on
by somebody with enough consumers - is essential
context for understanding why Java is the way that it is.

Many of Java's features are intended to give you ways
to minimize the number of observable properties of
the software you produce.

Private fields and methods are the easiest examples of this so far. If you
make fields or methods private then you can start to expect that
consumers of that class do not observe them. Thus, if needed, you
will not break anyone by changing them.[^setAccessible] 

[^setAccessible]: There are asterisks to this particular point, unfortunately.
There are ways to magically get at private fields like criminal scum.