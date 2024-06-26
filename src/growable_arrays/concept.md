# Concept

The concept behind a growable array is that we
store an array as a field and use it for operations like getting
and setting elements.

The extra wrinkle is that when someone wants to "add" an element
we make a new, bigger, array and copy all the existing elements to it.
Then we put the element you wanted to add at the end.

