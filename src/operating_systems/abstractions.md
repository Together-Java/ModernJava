# Abstractions

The most important jobs of an operating system is to "abstract"
over the hardware.

You shouldn't need to know what brand network card you have in order
to write code that connects to the internet. You shouldn't need to know
what kind of hard drive will be on the machine to store data.

We call these abstractions because they take things that are concrete,
like a dozen specific models of hard drive and the exact bits to send to do their operations, 
and make an "abstract model" of their commonalities.[^deeper]

This lets programmers write programs that will run on any machine that has the right operating system.
It doesn't help writing programs that will run on any operating system because different operating systems
provide different abstractions over the same hardware. The code to write to a hard drive in Windows is different than it is in Mac OS.

[^deeper]: There are deeper and shallower versions of this explanation which we will
get to. There will be plenty of time to talk about this concept as it relates to Java and other things.
