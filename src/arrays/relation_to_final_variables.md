# Relation to Final Variables

Just like anything else, arrays can be stored in variables marked `final`.

This means that the variable cannot be reassigned, but it does not mean
that the array's contents cannot be changed directly or through an alias.

```java
~void main() {
final char[] catchphrase = { 'w', 'o', 'a', 'h', '!' };
// woah!
System.out.println(catchphrase);

// Cannot reassign
// catchphrase = { 'e', 'g', 'a', 'd', 's' }
// but can set elements directly
catchphrase[0] = 'e';
catchphrase[1] = 'g';

// or through an alias
char[] alias = catchphrase;
alias[2] = 'a';
alias[3] = 'd';
alias[4] = 's';

// egads
System.out.println(catchphrase);
~}
```
