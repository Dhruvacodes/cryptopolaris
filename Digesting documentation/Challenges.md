# Learning from documentation

```bash
Connected!
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{czq09yVRY9Q67AO7DHoXq90pnOz.dRjM5QDL4ETN0czW}
hacker@man~learning-from-documentation:~$
```

# Learning Complex usage 

```bash
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{IBdPf33uvUZwkVlr7SqiZ8Wf9ky.dVjM5QDL4ETN0czW}
hacker@man~learning-complex-usage:~$ 
```

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

# Searching Manuals

```bash
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge  --jjkjle
Initializing...
Correct usage! Your flag: pwn.college{AMiZxDEOoBzQJSXHnXAZa-dp-Qr.dVTM4QDL4ETN0czW}
hacker@man~searching-manuals:~$ 
```

# Searching for manuals

```bash
hacker@man~searching-for-manuals:~$ man man
hacker@man~searching-for-manuals:~man -K challenge
hacker@man~searching-for-manuals:~$ /challenge/challenge --hqkvbb 683
Correct usage! Your flag: pwn.college{UJEhqWkv6bb8KZK3uU94NvuVBdG.dZTM4QDL4ETN0czW}
```
# Helpful Programs

```bash
hacker@man~helpful-programs:~$ /challenge/challenge --help
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 952
hacker@man~helpful-programs:~$ /challenge/challenge -g 952            
Correct usage! Your flag: pwn.college{M9WrEqT5XAJcVGUYwRTditV2z6E.ddjM4QDL4ETN0czW}
hacker@man~helpful-programs:~$ 
```

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
