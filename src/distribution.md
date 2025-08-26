# Distribution

If you are intending to run code on your own machine there isn't much reason to 
compile or package it. Compiling and packaging become useful when sharing
code with other developers or when "deploying" code to a machine you (in some manner) control.

But if you are making code intended to be used by a layperson it is insane to expect them
to install Java special just for your program. It can also become burden on you
since if you do get them to install Java, they won't keep it up to date.

The solution is to bundle your code with the Java runtime itself. This gives you
an "artifact" you can freely distribute and have someone "just run."
