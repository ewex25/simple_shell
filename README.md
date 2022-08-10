Simple Shell
---
![alt text](https://s3.amazonaws.com/intranet-projects-files/holbertonschool-low_level_programming/235/shell.jpeg)

## Name

hsh - a simple shell

## Description

this project recreates a simple command line shell that executes commands read from the standard input or from a file

* can execute any commands from the environment path
* works on interactive and non-interactive mode
* commands must be on a single line
* arguments must be separated by whitespace
* no quoting arguments and escaping whitespace
* no piping or redirection
* it doesn't handle aliases, comments or  history
* built-in commands:

  - env (print a list of the current environment variables)

  - exit (exits the shell)

##### Example 1 | cat command

```
$ cat environ.c
#include "shell.h"

/**
 * print_env - a function that prints the environment
 * Return: 0
 */

int print_env(void)
{
	int i = 0;

	while (environ[i])
	{
		/* prints in form of "variable=value" */
		write(1, environ[i], _strlen(environ[i]));
		i++;
		write(1, "\n", 1);
	}
	return (0);
}

$

```

##### Example 2 | BUILT-IN COMMAND: exit

```

vagrant@simple_shell$ ./hsh
$ echo Quitting the simple shell with the exit command
Quitting the simple shell with the exit command
$ exit
vagrant@simple_shell$

```

### List of allowed functions and system calls
* access (man 2 access)
* chdir (man 2 chdir)
* close (man 2 close)
* closedir (man 3 closedir)
* execve (man 2 execve)
* exit (man 3 exit)
* _exit (man 2 _exit)
* fflush (man 3 fflush)
* fork (man 2 fork)
* free (man 3 free)
* getcwd (man 3 getcwd)
* getline (man 3 getline)
* isatty (man 3 isatty)
* kill (man 2 kill)
* malloc (man 3 malloc)
* open (man 2 open)
* opendir (man 3 opendir)
* perror (man 3 perror)
* read (man 2 read)
* readdir (man 3 readdir)
* signal (man 2 signal)
* stat (__xstat) (man 2 stat)
* lstat (__lxstat) (man 2 lstat)
* fstat (__fxstat) (man 2 fstat)
* strtok (man 3 strtok)
* wait (man 2 wait)
* waitpid (man 2 waitpid)
* wait3 (man 2 wait3)
* wait4 (man 2 wait4)
* write (man 2 write)

---
File|Task
---|---
AUTHORS | the authors page
README.md | read me file
environ.c | prints the environment
error.c | handles errors
man_1_simple_shell | manual page
path.c | handles the PATH
shell.c | the main componenets of the shell
shell.h | the header file for the simple shell program
string.c | a series of functions to handle strings
tokenize.c | splits a string into tokens and count the number of tokens

#### Compilation

files should be compiled this way:

```$ gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh```

### Authors
-----------

[Ahmed Hassen](https://github.com/ewex25)

[Adewole Conde](https://github.com/phatboislym)
