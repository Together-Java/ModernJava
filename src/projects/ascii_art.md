# ASCII Art Generator

## Problem Statement

Humans like to draw stuff and to look at drawings of stuff.

We know this is in some manner intrinisic to us as a species
because we've found drawings in caves [dating back at least 51,200 years.](https://en.wikipedia.org/wiki/Cave_painting)

As such it is a normal impulse to use pictures, drawings, iconography, and other forms
of art as a tool for communication.

In the early days of the internet the amount of data you could send between computers was extremely limited.
This meant that, in practice, most people would communicate using solely text.

Instead of making it so that people couldn't send images to eachother, that restriction birthed a
new form of art. Using only the characters available to send as text, people would make and send pictures.

For example, here is a bat from [a website that archives examples of this form of art](https://www.asciiart.eu/animals/bats).

```
               /'.    .'\
               \( \__/ )/
         ___   / (.)(.) \   ___
    _.-"`_  `-.|  ____  |.-`  _`"-._
 .-'.-'//||`'-.\  V--V  /.-'`||\\'-.'-.
`'-'-.// ||    / .___.  \    || \\.-'-'`
      `-.||_.._|        |_.._||.-'
               \ ((  )) /
           jgs  '.    .'
                  `\/`
```

[Here are some cubes](https://www.asciiart.eu/art-and-design/geometries).

```
+------+.      +------+       +------+       +------+      .+------+
|`.    | `.    |\     |\      |      |      /|     /|    .' |    .'|
|  `+--+---+   | +----+-+     +------+     +-+----+ |   +---+--+'  |
|   |  |   |   | |    | |     |      |     | |    | |   |   |  |   |
+---+--+.  |   +-+----+ |     +------+     | +----+-+   |  .+--+---+
 `. |    `.|    \|     \|     |      |     |/     |/    |.'    | .'
   `+------+     +------+     +------+     +------+     +------+'
```

[And this one is a dog](https://www.asciiart.eu/animals/dogs).

```
          __
 \ ______/ V`-,
  }        /~~
 /_)^ --,r'
|b      |b
```

We call these drawings "ASCII Art" after the "American Standard Code for Information Interchange" - ASCII.
ASCII defined an English-centric set of characters and how to represent them in a computer. Much of this early
art was made solely using that character set, hence the name.

Even though sending images is now practical to do over the internet, ASCII art is still
a valid form of expression. Either as a deliberate choice or because of using a text only medium
(they still exist. Think of in-game chats.) ASCII art can be useful.

If you want to see how far this can be taken 
check out this [entirely ASCII art rendition of the Star Wars IV: A New Hope](https://www.asciimation.co.nz/index.php)



## Your Goal

Make a program that asks a user for a "height" and then prints out an ASCII art christmas tree
that is that many characters tall.

Here is an example tree you can use as a starting point. You can print this when asked for a height of `3`.

```
  *
 ***
*****
  |
```

Here is another example, but with a height of `5`.

```
    *
   ***
  *****
 *******
*********
    |
```

And here it is with a height of `1`

```
*
|
```




## Future Goals

When you learn enough to do the following, come back to this project and expand it.

* Draw something with more varied parts, like a snowman. You might find it convenient to not directly print to the screen, but instead "draw" what you want to print into an array first then print the contents of that array.

```
        ---
        | |
       -----
      / _ ^ \
      | * * |
      |  V  |
      \^___^/
      -------
     /       \
   * |       | *
  *  |       |  *
 *   |       |   *
*    \-------/    *
     ---------
    /         \
    |         |
    |         |
    |         |
    |         |
    \---------/
```
* Make sure that if the person using your program gives you a negative number, zero, or something that is
not a number you don't just crash. This means you might need to reprompt them for information.
* Make the christmas tree prettier. This will require "finding the pattern" in a more interesting piece of art, like [this example](https://www.asciiart.eu/holiday-and-events/christmas/trees).

```
      /\      
     /\*\     
    /\O\*\    
   /*/\/\/\   
  /\O\/\*\/\  
 /\*\/\*\/\/\ 
/\O\/\/*/\/O/\
      ||      
      ||      
      ||      
```

* Draw both the snowman and a tree. Let the user select which goes on the left and which goes on the right.

* Turn this into a command-line program that works similarly to the [cowsay](https://en.wikipedia.org/wiki/Cowsay#:~:text=cowsay%20is%20a%20program%20that,a%20cow%20with%20a%20message.) tool.

```
 _______
< Hello >
 -------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
```

* Expand or refocus into drawing other kinds of things.