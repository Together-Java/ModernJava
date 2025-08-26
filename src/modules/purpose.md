# Purpose

It might be a little unclear at first what reason
modules have for existing.

After all, don't packages already group code? Why would you
want groupings of a grouping?

The answer is that[^more] when you share code with other people
you will often want to have that code contain multiple packages.
If you couldn't "hide" packages of code from the people using
the code you are sharing it would be a bummer.

Just as private fields help you encapsulate state in a class
and package-private classes help you encapsulate whole classes,
unexported packages are your mechanism for encapsulating whole package.


[^andby]: And by "you" I mean you and whoever else is directly working with you.

[^more]: There are more answers, but they mostly involve tales of Java's past
and mistakes that were made there.