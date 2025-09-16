# Install Java

After you've got VSCodium set up the next step 
is to install Java.[^barebones]

## Chromebooks and School Computers

<details>
    <summary> Expand </summary>

You can skip this step. The instructions I gave to get set up with Github Codespaces
should have given you an environment where Java is already set up.

</details>


## Windows

<details>
    <summary> Expand </summary>

Download the "JDK MSI" from [adoptium.net](https://adoptium.net/temurin/releases/?version=25&os=windows).
Select whatever the newest version is. You will need at least Java 25 to follow along with the
examples in this book.

Run the installer, selecting all the default options. This should make the `java` command available to
you. 

</details>


## Mac OS

<details>
    <summary> Expand </summary>

Download the "JDK .pkg" from [adoptium.net](https://adoptium.net/temurin/releases/?version=25&os=mac).
Select whatever the newest version is. You will need at least Java 25 to follow along with the
examples in this book.

Run the installer, selecting all the default options. This should make the `java` command available to
you.

</details>

## Linux

<details>
    <summary> Expand </summary>

Linux is a little annoying. If you are using it you are likely used to it
by now, but you can use [adoptium.net](https://adoptium.net/temurin/releases/?version=25&os=linux) like everyone else, but there is no universal installer there.

You can either download the `.tar.gz` file that matches your machine, extract it,
and add the `bin` folder to your `PATH`, or you can try to find an installer for your
specific linux distribution.

</details>

[^barebones]: Apologies if you find these instructions a little barebones.