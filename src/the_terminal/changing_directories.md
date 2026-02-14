# Changing Directories

You can change what your working directory is using the `cd` command.

After the name of the command, you write the name of the directory you want to change in to.

```bash
$ pwd
/Users/emccue
$ cd Downloads
$ pwd
/Users/emccue/Downloads
```

If you want to go to a "parent" directory, you can write `..`. This means "one directory up".

```bash
$ pwd
/Users/emccue
$ cd ..
$ pwd
/Users
```

If you want to go to your "home" directory, you do not pass any arguments or write `~`.
```bash
$ pwd
/home/user/Documents
$ cd 
$ pwd
/home
```

[^cd]: Short for "change directory"
