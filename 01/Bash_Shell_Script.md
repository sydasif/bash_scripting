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
