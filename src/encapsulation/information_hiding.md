# Information Hiding

When encapsulating, your fundamental activity is finding
ways to hide information that you consider to be 
implementation details.

If you did not hide this information and
you have a large number of consumers[^if], you would never
be able to change those implementation details.

Something to be careful of with respect to this is "side channels."
If you use the mechanisms Java gives you to hide a field from people,
..

[^if]: Again, if. These concerns do not apply as much to 
programs written at smaller scales or programs written
_within_ some encapsulation boundary. Don't get too paranoid
about needing to hide things.