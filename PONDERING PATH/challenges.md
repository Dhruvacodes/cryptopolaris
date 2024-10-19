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
PATH variable is where all the executables are stored. So if the rm command is not found, the flag file cannot be removed.

