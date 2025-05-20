# Coupling

<!-- https://www.youtube.com/watch?v=rQlMtztiAoA -->

If two things are "coupled" it means that a change in one
will mandate a change in the other. Or, at the very least,
active consideration of whether such a change is neccesary.

In a way "coupling" is the opposite of "abstraction." Instead
of hiding implementation details you freely intermingle them.

This does not mean that coupling is bad. On the contrary, so
long as code that is coupled is also "co-located" making changes
to that code can be easier than if it were spread over multiple files.

A not insignificant part of practice in the coding world is deciding when
pieces of a program deserve to be abstracted from eachother (to minimize interdependence)
and when they deserve to be coupled together (to keep logic in one place.)