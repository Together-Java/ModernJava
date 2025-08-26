# Implicit Interfaces

There are many kinds of "interfaces."

There are `interface`s the Java language construct - these let you 
specify methods that different classes will share and write code
that will work against anything which implements that interface.

But there are also "interfaces" that you encounter in the real world.
The classic example is an automobile. Once you understand
the "interface" of a steering wheel, brake pedal, and gas pedal
you can drive most any car.

Then back within Java there are things which form "an interface"
which may or may not use the `interface` keyword. The static methods available on a class,
the constructors that are public, the set of classes that come with a library, etc.

I think a more general concept is "the implicit interface." Everything you can observe about a thing forms its "implicit interface."[^implicit]

[^implicit]: I call it "implicit" because there is no place where you write down "all the properties of a thing" that is not the thing itself. And by thing I mean field, method, class, group of classes, package names - everything.