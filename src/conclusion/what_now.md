# What Now?

If you have made it this far:

1. Congratulations, you have now learned Java!
2. You are probably wondering what you should do next.

## Go Deeper

No matter how much I write there is no chance I will have covered all of the Java
language nor all of what you might want to know to write software in Java.

With what you've learned so far you should have a solid enough foundation
to go off and learn from other sources. I'll try and paint a picture of the landscape for you
before you run off though.

### Build Tools

First you probably are going to want to learn a build tool.
I haven't covered how to get dependencies yet and that is on purpose.

In the Java world - due to the ability to launch a program with `java src/Main.java` being
a pretty recent development - all the tools that help you automatically download
libraries written by other people are married with tools that "build" - i.e. run `javac`, `jar`, etc.
for you - your code.

There are two major build tools (meaning widely used) in the Java world (Maven and Gradle)
as well as many more niche ones (bld, mill, etc.).

If you want a gentle introduction to this world you can start with bld, though be aware this
will be a road less travelled.

([bld tutorial here](https://github.com/rife2/bld/wiki))

If you want to learn the one that will probably be the most useful to you
in a professional setting you should learn Maven first.

(["Maven By Example" book here](https://books.sonatype.com/mvnex-book/reference/index.html))

If you are angling to get into Android development you should learn Gradle.
Hop ahead and check out the resources for Kotlin too because Kotlin is the
language you will use for Gradle build scripts.

([Gradle Documentation Here](https://docs.gradle.org/current/userguide/userguide.html))

### Minecraft

<img src="/conclusion/minecraft_duke.png" height="200px"/>

If your age begins with the number `1` you are either near death or statistically
very interested in Minecraft.

A lot of people who learn Java do so in order to be able to write Minecraft
mods or plugins for Minecraft servers, it is normal.

Just a few words of caution:

* The world of Minecraft development can be deeply exploitative. If you are not
a full adult please do not try to "work" for anyone. Be careful. Talk to a
parent or an adult you trust when people online seem to want something from you.
* The kinds of code you write to make mods work will be pretty different than the
kind of code you would write for most other kinds of software. This is partially
because of what modding is (adjusting software whose evolution you do not control)
and partially because of peculiarities around Minecraft in particular.

With that all said: there are two basic "mod compatibility layers." These are
"Fabric" and "Forge."

The point of these is to give you code to program against that isn't the direct Minecraft source
code, which can change very frequently, and to give your mod a fighting chance of being compatible
across multiple Minecraft versions.

Of the two: this book probably prepared you the best for Forge. 

Forge requires you to use Gradle which in turn will require at least a little knowledge of Kotlin.
You don't need to take a full detour through that to get started, but you should put both of
those on your list of things to learn.

[Forge Getting Started here](https://docs.minecraftforge.net/en/latest/gettingstarted/)

["Modded Minecraft" Discord here](https://discord.gg/moddedmc)

["Minecraft Mod Development" Discord here](https://discord.com/invite/wpMz4AtAhn)

Fabric pretty quickly requires you to interact with a concept called a "Mixin."
This is a mechanism the Minecraft modding world made for magically editing the code inside Minecraft
among other things. If you go this path just be ready for that.

[Fabric Getting Started here](https://docs.fabricmc.net/develop/getting-started/introduction-to-fabric-and-modding)

[Fabric community Discord here]([https://discord.gg/v6v4pMv](https://discord.gg/v6v4pMv))

For making plugins that run on a custom Minecraft server - so things that handle custom
chat commands and things of that nature - you have to use the plugin required by whatever
server you are using. I am not the most up to date with Minecraft, but I know there
is both Spigot and PaperMC. I have been told that Spigot is the preferred option
as it allows for Bedrock players to play as well.

[Docs for Spigot here](https://www.spigotmc.org/wiki/spigot-plugin-development/)

[Spigot community Discord here](https://discord.gg/spigotmc)

[Docs for PaperMC here](https://docs.papermc.io/)

[PaperMC community Discord here](https://discord.gg/papermc)


### Websites

Making websites is a profitable career path. At least it is at the time of writing.
There are a few essential things you will need to learn about to get started with that
path.

The first is how to make an HTTP Server. HTTP Servers are what web browsers talk
to in order to render websites.

There are a lot of tools for this in Java. A lot a lot. I would recommend
starting with the one that comes built-in: the `jdk.httpserver` module.

[Docs for `jdk.httpserver` here](https://docs.oracle.com/en/java/javase/24/docs/api/jdk.httpserver/module-summary.html)

Then you will need to learn about SQL databases and how to query from/insert into them from Java.

A good start for that is SQLite - it is a database that runs self-contained in a single file.

[SQLite tutorial here](https://www.sqlitetutorial.net/)

After that - or as part of that - you should learn about JDBC. This is the way you interact with
a database from Java. 

[I have a primer for that here](https://mccue.dev/pages/1-17-24-java-sql)

Then from there you should learn about Dependency Injection

[Good video on that here](https://www.youtube.com/watch?v=J1f5b4vcxCQ)

And finally you can dive into the world of Spring - which is likely the
most employable one of the many HTTP server options out there.

[Spring Academy Courses here - the basic ones are free](https://spring.academy/)

### Desktop Applications

If you want to learn how to make desktop applications in Java you have basically
three paths.

Path #1 is to learn Java Swing. This is an old crusty GUI framework that is kinda difficult to use
but has the pro of coming with Java and being able to run on every potato in existence.

[Docs for `java.desktop` (Swing) here](https://docs.oracle.com/en/java/javase/24/docs/api/java.desktop/module-summary.html)

Path #2 is the learn JavaFX. By all accounts JavaFX is better software than Swing, but it was cursed
by coming out at a point in history where desktop apps were no longer big business to develop. It
was eventually removed from the JDK and you will need to procure it like any other dependency.

[Docs for JavaFX here](https://openjfx.io/openjfx-docs/)

## Learn a New Language

An unfortunate truth is that you cannot use Java for everything.

Sometimes this is intrinsic - Java would not be a good choice for code
driving a pacemaker - and some of it is just how the ecosystems around languages
are right now.

Even if you could get away with only using Java, there is significant value in knowing multiple
languages. Particuarly languages that are different than Java.

### JavaScript

<img src="/conclusion/javascript_mascot.png" height="200px"/>

To make highly interactive programs that run inside a browser you
will need JavaScript. JavaScript and languages that compile to JavaScript 
are basically the only language it is practical
to use for the frontend of a website[^wasm].

It is probably worth your time to learn how to write JavaScript.

[Mozilla Developer Network's JavaScript Guide here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)

The most popular language that compiles to JavaScript is TypeScript. After you've
learned JavaScript that is a good one to touch next.

[TypeScript tutorial here](https://www.typescripttutorial.net/)


There are languages out there like TypeScript that compile to JavaScript -
and you can find some projects out there that do much the same for Java -
but just practically speaking learning JavaScript is going to be something
you have to do at some point if you get into making websites.

### C#

<img src="/conclusion/csharp_mascot.png" height="200px"/>

C# is a language broadly similar to Java. It has a lot of features Java doesn't - for better or worse -
but the basics are comparable.

C# is very prevalent in the game development world. The Unity game engine, 
[corporate blunders notwithstanding](https://www.theverge.com/2024/9/12/24242937/unity-runtime-fee-cancelled-subscription-pricing), is still very big and still has you use C# for game scripts. Competitors like Godot [have C# Scripting as well](https://docs.godotengine.org/en/stable/tutorials/scripting/c_sharp/index.html).

You will also find C# being used to make websites and desktop apps but it doesn't have
as much unique pull there as it does in game development.

[Microsoft's C# tutorial here](https://learn.microsoft.com/en-us/training/paths/get-started-c-sharp-part-1/)

### Kotlin

<img src="/conclusion/kotlin_mascot.png" height="200px"/>

Kotlin is one of a family of languages that try to be a "better Java."
Better is relative, but you are likely to learn _something_ when diving into it.

Regardless, Kotlin is what you nowadays use to write Gradle build scripts in and
Kotlin is the de-facto language for writing Android apps.

This means that, while Java in some form is still technically an option,
all the documentation for Android will be using Kotlin for their examples
and most new frameworks will assume you are using Kotlin in preference to Java.

And Gradle is a build tool that many Java projects choose to use. You probably don't need
as deep of an understanding of Kotlin to work with Gradle build scripts as
you do to make a full app in it, but it can't hurt.

[Getting Started with Kotlin tutorial here](https://kotlinlang.org/docs/getting-started.html)

[Kotlin Android Tutorial here](https://kotlinlang.org/docs/android-overview.html)

If you want to make Desktop, Mobile, or Web apps in Kotlin it is probably also worth checking out
Jetbrains Compose Multiplatfrom.

[Getting Started for Jetbrains Compose Multiplatfrom here](https://www.jetbrains.com/help/kotlin-multiplatform-dev/compose-multiplatform-create-first-app.html)


### Others

Other languages you might want to learn that I haven't written up
context for quite yet:

* C

<img src="/conclusion/cici_c_rat.png" height="200px"/>

* C++
* Clojure
* Elm
* Haskell
* Python

<img src="/conclusion/python_logo.png" height="200px"/>

* Ruby


<img src="/conclusion/ruby_logo.png" height="200px"/>

* Go


<img src="/conclusion/go_mascot.png" height="200px"/>

* Rust
* Zig
* Clojure


[^wasm]: Fight me, WebAssembly fans.