# 0x16. C - Simple Shell

![alt text](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQk-Toji9YT0iWdnw8c2yHFI2_fVMQcjGVndw&usqp=CAU)

## Description

Simple_shell is an sh-compatible command language interpreter that executes commands read from the standard input or from a file.

The simple_shell is a command that reads lines from either a file or the terminal, interprets them, and generally executes other commands. The simple_shell implements a language that has flow control constructs, a macro facility that provides a variety of features in addition to data storage, along with built in history and lineediting capabilities. It incorporates many features to aid interactive use and has the advantage that the interpretative language is common to both interactive and non-interactive use(shell scripts). That is, commands canbe typed directly to the running shell or can be put into a file and the file can be executed directly by the shell.

## Syntax

The shell works by using commands given by the user input. The shell commands take in the following syntax:
```
#cisfun$ <command> <flags or options> <argument 1> <argument 2> ...
```

## Feautres

*Displays a prompt and waits for user to type a command
*Can handle commands with options and arguments
*Prompt displays again each time command is executed
*Uses PATH variable to find executable command
*If executable is not found, prints an error message and displays prompt again
*Includes an exit function that exits the shell
*Includes an env built-in that prints the current environment

## Usage

*Enter custom shell by typing "./hsh". You should be prompted with a #cisfun$
*Type a command of your liking and press "Enter"
*Appropriate output will appear
*Prompt reappears and awaits your next command
*Exit shell by typing "exit" o "ctrl D"

## Environment

The custom shell was developed and tested on ``Ubuntu 14.04`` LTS via Vagrant in VirtualBox.

## Compilation

All files will be compiled with the following:
```
gcc -Wall -Werror -Wextra -pedantic *.c -o hsh
```
## Exiting commands and the shell

To exit out of a command or process the user can use ctrl c. Control c stops a process and causes it to abort. The user can also utilize the command ctrl D which will just exit. When the command ctrl D is used an exit status of 0 is given. Using exit, you can input its exit status or it is defaulted to thestatus of the last command executed.

## Example

Interactive Mode
```
 $ ./hsh
($) /bin/ls
hsh main.c shell.c
($)
($) exit
 $
```
Non-interactive Mode
```
$ echo "/bin/ls" | ./hsh
hsh main.c shell.c test_ls_2
$
$ cat test_ls_2
/bin/ls
/bin/ls
$
$ cat test_ls_2 | ./hsh
hsh main.c shell.c test_ls_2
hsh main.c shell.c test_ls_2
$
```
Akijibade Fortunate [GitHub](https://github.com/G-badek)
