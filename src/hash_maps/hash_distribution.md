# Hash Distribution

When picking a hash function you also need to be worried
about "hash distribution."

If you open up a doctor's office in South Boston, you might have an issue
ordering charts by last name only. Your `M` cabinet will be overflowing.[^irish]

For that scenario, using the first letter of the last name is a non-ideal hash function
because so when many people have last names starting with the same letter, they will
not be evenly distributed amongst the buckets.

Making a hash function with a good distribution is hard. `Objects.hash` will do a decent job of it
and thats why we use it.

[^irish]: "Mc" and "Mac" are common irish surnames and Boston has a sizable irish population.