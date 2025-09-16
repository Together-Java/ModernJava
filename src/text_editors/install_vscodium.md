# Install VSCodium

To install VSCodium you need to go to this page:

[https://github.com/VSCodium/vscodium/releases](https://github.com/VSCodium/vscodium/releases).

Then follow the instructions below specific to what kind of computer you have.

## Chromebooks and School Computers

<details>
    <summary> Expand </summary>
    <p>Unfortunately the defining characteristic of a Chromebook is that you cannot install
    "normal" software on it.</p>
    <p>This is also generally true for computers provided to you by a school. Sometimes they will
    be okay with you running things normally, sometimes not.</p>
    <p>For these situations VSCodium is not an option so for now I am going to recommend falling
    back to using a service called "Github Codespaces." This is a service provided by Microsoft
    where they let you use VSCode in a web browser.</p>
    <p> First, <a href="https://github.com/">make an account on Github</a>.</p>
    <p> Then go to <a href="https://github.com/bowbahdoe/j25-codespace"> https://github.com/bowbahdoe/j25-codespace</a> and press the <code>.</code> key on your keyboard.</p>
    <img src="/text_editors/codespace_repo_landing.png"></img>
    <p> After pressing <code>.</code> you should be redirected to a page that looks like this </p>
    <img src="/text_editors/codespace_first_view.png" />
    <p> Click the button on the bottom labeled "Continue Working in GitHub Codespaces."</p>
    <img src="/text_editors/codespace_continue_working.png" />
    <p> Select the smallest instance size from the dropdown that appears. </p>
    <img src="/text_editors/codespace_instance_size.png" />
    <p> After it loads for awhile you will see a pop-up in the bottom left of your screen asking
    if you want to install an extension for Java files. </p>
    <img src="/text_editors/codespace_extension_prompt.png" />
    <p> You want to say no to this. </p>
    <img src="/text_editors/codespace_extension_no.png" />
    <p> You will also want to say no to all extension suggestions. </p>
    <img src="/text_editors/codespace_ignore_all.png" />
    <p>Next on the chopping block is the AI thing on the right. You want to uncheck the "Show View by Default." option on it then click the `x` to dismiss it.</p>
    <img src="/text_editors/codespace_ai.png" />
    <p>After vanquishing evil, your next task is to type `java src/Main.java` into the "Terminal" area at the bottom of your screen.</p>
    <img src="/text_editors/codespace_srcmainjava.png" />
    <p>Press the enter key and you should see "Hello, world" be printed out.</p>
    <img src="/text_editors/codespace_run_code.png" />
    <p>You can skip the next section on installing Java for now. You are ready to proceed with the book.</p>
</details>
    

## Windows

<details>
    <summary>Expand</summary>
If you are on Windows you want to click this link.
</details>

## MacOS

<details>
    <summary>Expand</summary>
    <p>If you have an Apple M1 Mac or newer then you need to scroll down
to the "ARM 64bits" section (of whatever the newest release is) and click this link.</p>

<img src="/text_editors/mac_arm_download.png" />

<p>If you have an older Mac then you want to click this link.</p>

<img src="/text_editors/mac_x86_download.png" />

<p>This will download a file. Double click it and it will open a window like this.</p>
<img src="/text_editors/mac_vscodium_dmg_open.png" />

<p>Then drag the VSCodium logo to the Applications folder.</p>
<img src="/text_editors/mac_vscodium_dmg_drag.png" />

<p>Then you should be able to find and open the app from the Launchpad app.</p>

<img src="/text_editors/mac_launchpad.png" />

<img src="/text_editors/mac_launchpad_vscodium_search.png" />

<p>When you open it you should see a screen like this.</p>
<img src="/text_editors/mac_blank.png" />

<p>In the top-right corner select File -> Open Folder </p>
<img src="/text_editors/mac_open_folder.png" />

<p>Make a folder somewhere on your computer to store your code. It doesn't matter what you call it.</p>
<img src="/text_editors/mac_new_folder.png" />

<p>Then make a new file named <code>src/Main.java</code></p>
<img src="/text_editors/mac_new_file.png" />
<img src="/text_editors/mac_make_file.png"/>

<p>Inside of this file put the following contents. </p>

```java,no_run
void main() {
    IO.println("Hello, world");
}
```

<p> Now skip ahead to the next section on installing Java. Come back when you are done. </p>

<p> Once you are back you want to open a new terminal. </p>

<img src="/text_editors/mac_new_terminal.png"/>

<p> Type <code>java src/Main.java</code> in the terminal and press enter to run your first program.
If this doesn't work you might need to restart your computer or you might have messed up a step.</p>

<img src="/text_editors/mac_run_java.png"/>

</details>

## Linux

<details>
    <summary>Expand</summary>
    <p>Select the installer that matches your system and go from there.</p>
    <p>Sorry I don't have as nice of a walkthrough as I do for Windows and Mac. In my defense,
    every Linux machine is its own beast.</p>
</details