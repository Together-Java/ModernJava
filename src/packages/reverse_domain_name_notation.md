# Reverse Domain Name Notation

Part of the point of putting classes into packages
is to avoid conflicts when using code written by other people.

If you want a class named `RiceCooker` and you want to use a code that someone
on the internet wrote which just so happens to also have a class named `RiceCooker`,
that only works if you both put your classes in different packages.

Making sure different people cooperate is a hard problem, so the social convention
that emerged was to name packages using a "reverse domain name notation."

Only one person could own a domain name - like `google.com` - at a time. So all
code coming out of Google[^shared] would start with a package name which is the reverse
of that - `com.google`.[^thisiswhy] 

Nowadays people also tend to accept unique prefixes based on accounts you might have on a site. So you might see things like `com.github.their_username_here` for people who have an account with a service like `Github`.

It isn't perfect, nothing would be, but its socially dominant so you should be aware of it. If the code being written is for an application and won't be shared with others you do not need to do this sort of thing yourself.


[^shared]: That might be mixed with other code written by different companies or by different people.
[^thisiswhy]: This is why many tools will have your starter project have classes in the `com.example` package