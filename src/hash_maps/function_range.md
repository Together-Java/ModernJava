# Function Range

Once you have a hash function, you need to determine its range.

The range of a function is the set of values it might return.

If you have a function that might return any `int` then the range will be
all the values between `Integer.MIN_VALUE` and `Integer.MAX_VALUE`.

If your hash function only returns a number between `0` and `5`, `0` - `5`
is the range.
