# 02: Variables in Bash Shell Scripting

If you never worked with variables before, you can think of them as a container that stores a piece of information that can vary over time.

Variables always come in handy while writing a script and in this tutorial, you will learn how to use variables in your bash scripts.

## Using variables in bash shell scripts

That was a simple Hello World script. Let's make it a better Hello World.

```shell
#!/bin/bash

echo 'Hello, World!'
```

Let's improve the script by using shell variables so that it greets users with their names. Edit your hello.sh script and use read command to get input from the user:

```shell
#!/bin/bash

echo "What's your name, stranger?"

read name

echo "Hello, $name"
```
