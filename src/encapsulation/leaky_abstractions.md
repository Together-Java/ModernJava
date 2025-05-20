# Leaky Abstractions

If an abstraction doesn't fully encapsulate what it is trying to we call
that abstraction "leaky."

As an example, say we define a person as having a first name and a given name. That
might work for a large number of people. But the moment our program needs to represent
Plato, who did not have a given name, that abstraction "leaks."

Now suddenly the code that would work with people needs to account for an "empty" given name
where it didn't before and we need to pick a special value to represent such a name (empty string or `null` generally). The abstraction has leaked.

There are maybe more illuminating examples, but thats the general concept. Its not the end of the
world if an abstraction leaks. It might just be a sign of a changing world or of not having thought through a problem fully. You can adapt to that. It's just worth knowing about.