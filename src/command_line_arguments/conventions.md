# Conventions

As it is just a `String[]`, you can interpret the arguments passed to your
program in any way you choose.

What you will notice, however, from using other tools in your terminal
is that there are a few socially accepted conventions.

If your tool takes "options" then you would expect `--option-name VALUE` to
be how you specify it. So two dashes followed by the argument name.

If you need a shorter version then you allow for one dash and sometimes a single
letter value `-d VALUE`.

And most importantly, if someone types `--help` you should give them the
available options. Try `java --help` for an example.

