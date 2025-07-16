# Modern Java

[![codefactor](https://img.shields.io/codefactor/grade/github/together-java/modernjava)](https://www.codefactor.io/repository/github/together-java/modernjava)
[![license](https://img.shields.io/github/license/Together-Java/ModernJava)](https://github.com/Together-Java/ModernJava/blob/master/LICENSE)

Greetings.

This is a book intended to teach someone the Java language, from scratch. 

You will find that the content makes heavy use of recently released and, for the moment,
preview features. This is intentional as much of the topic ordering doesn't work
without at least Java 21.

Right now I have several key areas where I could use some help:

* Writing Challenges. Most of the early sections have challenges students can do to test
their understanding of the topics covered and for practice. I've shifted my focus away from
these to make more progress on the main content of the book. Any assistance would be appreciated.
* Theming. A lot of the chapters are...bland. Purely technical. I find that when I have the imagination to "theme" the subjects they become higher quality and more engaging overall. See
an anime you liked recently and think you can make the math chapters use the characters from it?
Give it a shot!
* Fixing Mechanical Issues. I don't have an editor and I don't often proofread. If you find mechanical errors
in my grammar or find issues with the way topics are ordered I would welcome fixes.

Notably I do not want to open the floodgates for contributions on the main chapter content
just yet. This has the downside of slower progress but the upside of a more coherent result.

My primary goals with this are

* Get the ordering of topics right. By this I mean that every topic covered should have had its pre-requitsites covered in the topics previous. While "lesson 1: Inheritance" is clearly wrong
in this regard, some things are more subtle.
* Be a template for other people. This is a book. Not everyone likes books, some like youtube videos, some like over priced udemy courses, some attend College, etc. Everyone has different learning paths. I hope this to be of use to anyone looking to make a more up to date Java
curriculum and hope that the vague order of things (which I consider superior to the content
produced with the Java of years' past) as carried through.
* Write as if the newest Java wasn't new. Its obvious when a book was written before Java 8
because it always has newer additions with "addendum: brand new stuff in Java 8." But 
the order language features were introduced is hardly a good order to teach them. You have
to pretend that Java 21 has always been *the* Java. Does it really make sense to show terrible
C-style switch statements way before switch expressions?
* Write as if the words Object Oriented Programming, Functional Programming, etc. didn't exist.
While I understand that these all have definitions and are useful concepts to know about, introducing them early seems to lead to either dogma, rejection of said dogma, or some
mix thereof. None of them are actually needed to understand the mechanics of and motivation
behind what we would call "object oriented" or "functional" techniques. They certainly don't
work as justification for adding getters and setters to every class.

Feel free to join our [discord server](https://discord.gg/together-java-272761734820003841)
if you have any questions, or require assistance with the project.

## Getting started

Please read [Contributing](https://github.com/Together-Java/ModernJava/wiki/Contributing)
guidelines if you are considering helping us out! There you will find a detailed
guide on how to contribute, and plenty of resources in case this is your
first time submitting a PR to an open-source project.

Head over to the [Wiki](https://github.com/Together-Java/ModernJava/wiki) as general
entry point to the project. It provides lots of tutorials, documentation and other information.

To run this locally you will need `mdbook`. The instructions for doing so are [here](https://rust-lang.github.io/mdBook/guide/installation.html).

Then just run the following.

```
mdbook serve
```
