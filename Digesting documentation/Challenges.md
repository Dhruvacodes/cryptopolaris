# Learning from documentation

```bash
Connected!
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{czq09yVRY9Q67AO7DHoXq90pnOz.dRjM5QDL4ETN0czW}
hacker@man~learning-from-documentation:~$
```
Here we learnt how to give arguments. 
The format for giving arguments can be <filename> -- argument

# Learning Complex usage 

```bash
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{IBdPf33uvUZwkVlr7SqiZ8Wf9ky.dVjM5QDL4ETN0czW}
hacker@man~learning-complex-usage:~$ 
```
Here we went one step ahead.
-- printfile was already an argument and we gave it another argument which in this case is the path of the flag to be read.

# Reading manuals 

```bash
Connected!                                                                        
hacker@man~reading-manuals:~$ man challenge

CHALLENGE(1)                                    Challenge Commands                                   CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --gjdgun NUM
              print the flag if NUM is 116

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-luminarium/>

SEE ALSO
       man(1) bash-builtins(7)

pwn.college                                          May 2024                                        CHALLENGE(1)
hacker@man~reading-manuals:~$ /challenge/challenge --gjdgun 116
Correct usage! Your flag: pwn.college{MgXj_dg1u1nNahoyUjMb6uCY-se.dRTM4QDL4ETN0czW}
hacker@man~reading-manuals:~$ 
```
The purpose of this question was to teach us the man command.
The man command is short for manual and is used to access manual of the argument.

# Searching Manuals

```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge  --jjkjle
Initializing...
Correct usage! Your flag: pwn.college{AMiZxDEOoBzQJSXHnXAZa-dp-Qr.dVTM4QDL4ETN0czW}
hacker@man~searching-manuals:~$ 
```
Used the ? command to find out the correct argument to find the flag
This argument is important because say for example in this case, I had 1694 lines which is impossible to go through manually, thus we need a command to find required text instantly.

# Searching for manuals

```bash
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~man -K challenge
hacker@man~searching-for-manuals:~$ /challenge/challenge --hqkvbb 683
Correct usage! Your flag: pwn.college{UJEhqWkv6bb8KZK3uU94NvuVBdG.dZTM4QDL4ETN0czW}
```
This was a complex program but the commands were easy.
Basically we had to use the man command for man to find other manuals.
After finding a relevant module we had to find the valid argument from it to find the key.

# Helpful Programs

```bash
hacker@man~helpful-programs:~$ /challenge/challenge --help
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 952
hacker@man~helpful-programs:~$ /challenge/challenge -g 952            
Correct usage! Your flag: pwn.college{M9WrEqT5XAJcVGUYwRTditV2z6E.ddjM4QDL4ETN0czW}
hacker@man~helpful-programs:~$ 
```
used the help argument to find information about challenge
then used given argument -p to find value for argument
finally used -q as argument for fiding the flag

# Help for Builtins

```bash
hacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune		display a fortune
      --version		display the version
      --secret VALUE	prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "g6RLVf7M".
hacker@man~help-for-builtins:~$ challenge --secret g6RLVf7M
Correct! Here is your flag!
pwn.college{g6RLVf7MiPFJJw0Gm7YMoMaQ0Xc.dRTM5QDL4ETN0czW}

hacker@man~help-for-builtins:~$ 
```
Learnt about builtin commands. 
Shell builtins are functions that are stored within the shell.
Used help challenge to find builtins in challenge.
Then used the correct argument to find the flag.
