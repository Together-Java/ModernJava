# Low Level versus High Level

TCP over IP, and by extension Sockets, are generally
considered to be a "low level" mechanism.

When we say something is "low level" its usually in reference to
a "high level" thing that is built on top of the lower level thing.
In the case of TCP over IP, there are multiple protocols that use it
behind the scenes but don't generally require a programmer
to know some of the finer details of how that is used.

We will get to a few of these eventually, but I bring this up
mostly to try and break the cultural taboo of using a low level
thing. There is a cultural bias in the programming field to prefer
higher levels mechanisms. This can sometimes be well-founded
but just as often be conditional on the situation.

Which is all to say, if someone mocks you for using sockets directly
don't feel bad about yourself. We are building up slowly for a reason.