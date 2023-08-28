# Accuracy

Floating Point numbers are not an exact representation of numbers.

The reasons for this are twofold.

1. It is much more efficient for a computer to work with data that is a "fixed size". You can't cram all the infinite possible
   numbers into 32, 64, or any fixed number of bits.
2. For most systems, the inaccuracy is okay. When it is not, there are ways to do "real math" that we will cover much later.

<!-- TODO: Cover BigInteger and BigDecimal and link back here. -->
<!-- TODO: Write an actual explanation and don't defer to computerphile. -->

For an explanation of the mechanics, I'll defer to this old Computerphile video.

<iframe width="560" height="315" src="https://www.youtube.com/embed/PZRI1IfStY0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
