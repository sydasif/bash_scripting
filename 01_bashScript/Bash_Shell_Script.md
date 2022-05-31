# 01: Create and Run Your First Bash Shell Script

## Run your first shell script

Create a new file named _hello.sh_ using the cat command:

```terminal
cat > hello.sh
```

Insert the following line in it by typing it in the terminal:

```terminal
echo 'Hello, World!'
```

Press _Ctrl+D_ to save the text to the file and come out of the cat command.

You can also use a terminal-based text editor like Vim, Emacs or Nano.

We are using the echo command to print _"Hello World"_. You can use this command in the terminal directly but in that, we run this command through a shell script.

Now make the file _hello.sh_ executable by using the chmod command as follows:

```terminal
chmod u+x hello.sh
```

And finally, run your first shell script by preceding the _hello.sh_ with your desired shell “bash”:

```terminal
bash hello.sh
```

You'll see Hello, World! printed on the screen.

```terminal
➜ bash hello.sh 
Hello, World!
```

## Convert your shell script into bash script

## The SheBang line at the beginning of shell script

The line “#!/bin/bash” is referred to as the shebang line and in some literature, it’s referred to as the hashbang line and that’s because it starts with the two characters hash ‘#’ and bang ‘!’.

```terminal
#!/bin/bash

echo 'Hello, World!'
```

When you include the line “#!/bin/bash” at the very top of your script, the system knows that you want to use bash as an interpreter for your script. Thus, you can run the hello.sh script directly now without preceding it with bash.

## Adding your shell script to the PATH

You may have noticed that I used _./hello.sh_ to run the script; you will get an error if you omit the leading ./

```terminal
hello.sh
hello.sh: command not found
```

Bash thought that you were trying to run a command named _hello.sh_. When you run any command on your terminal; they shell looks for that command in a set of directories that are stored in the PATH variable.

You can use echo to view the contents of that PATH variable:

```terminal
echo $PATH
/home/user/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
```

The colon character (:) separates the path of each of the directories that your shell scans whenever you run a command.

Linux commands like echo, cat etc can be run from anywhere because their executable files are stored in the bin directories. The bin directories are included in the PATH. When you run a command, your system checks the PATH for all the possible places it should look for to find the executable for that command.

If you want to run your bash script from anywhere, as if it were a regular Linux command, add the location of your shell script to the PATH variable.

First, get the location of your script's directory (assuming you are in the same directory), use the PWD command:

pwd

Use the export command to add your scripts directory to the PATH variable.

```terminal
export PATH=$PATH:/home/user/scripts
```

Notice that I have appended the 'scripts directory' to the very end to our PATH variable. So that the custom path is searched after the standard directories.
The moment of truth is here; run hello.sh:

```terminal
hello.sh
Hello, World!
```
