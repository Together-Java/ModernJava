# Exception

The most vanilla[^vanillacopypasta] checked exception is `Exception`.

If you want a checked exception and do not know of a better one, `Exception` will do.

```java,panics
void main() throws Exception {
    throw new Exception("Crash!");
}
```

[^vanillacopypasta]: <i>people have the audacity to equate vanilla with “plain”. the fruit of a delicate orchid pollinated by hand. worth its weight in solid gold and beyond. the fussy black-and-cream jewel of the american continent. you sick son of a bitch. imagine a world without vanilla. no blondies. no pound cakes. no crème brûlée, no coke floats. no cream soda. no satiny new york-style cheesecakes. no warm apple pie à la mode. no velvety complexity to bring out complex notes in chocolate desserts. no depth of flavour in your cakes and cookies and milkshakes. all in just a few precious seeds or grams of paste or perfumed teaspoons of liquid black platinum. what you don’t understand could fill the library of alexandria seven times over and then some. you ungrateful bastard i’m going to kill you</i> - [Tumblr user "kirbyofthestars"](https://www.tumblr.com/peaceoutofthepieces/684810307611377664)