# Hash Collision

It is possible for a hash function to give the same
result for two distinct elements. 

The first letter of both
"Smith" and "Sanders" is "S", so if the hash function takes the first letter
of the last name they will have the same hash.

We call this situation a "hash collision." All it means is that these two objects
will definitely go into the same bucket.

That's allowed to happen, but if _everything_ goes into the same bucket then there
isn't much point to using a `HashMap` over an `ArrayList`.