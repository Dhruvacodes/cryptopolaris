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

# 4) Hijacking commands

```bash
hacker@path~hijacking-commands:~$ echo /usr/bin/cat /flag > rm
hacker@path~hijacking-commands:~$ chmod u+x rm
hacker@path~hijacking-commands:~$ PATH="/home/hacker"
hacker@path~hijacking-commands:~$ /challenge/run
Trying to remove /flag...
pwn.college{sanpZYet1GQYrcursgDsp-vy307.ddzNyUDL4ETN0czW}
```

