# 1) Listing processes.

```bash
hacker@processes~listing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 04:29 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bin/dojo-init /run/dojo/bin
root           7       1  0 04:29 ?        00:00:00 /run/dojo/bin/sleep 6h
root          68       1  0 04:29 ?        00:00:00 /challenge/18049-run-26186
root          72      68  0 04:29 ?        00:00:00 sleep 6h
hacker        73       0  0 04:29 pts/0    00:00:00 /run/dojo/bin/ssh-entrypoint
hacker        90      73  0 04:29 pts/0    00:00:00 ps -ef
hacker@processes~listing-processes:~$ /challenge/18049-run-26186
Yahaha, you found me! Here is your flag:
pwn.college{YdQmQ-JxzObMRubNTYUpkYEbkDo.dhzM4QDL4ETN0czW}
Now I will sleep for a while (so that you could find me with 'ps').

```
The ps -ef and ps aux commands are used to list the processes currently running in the terminal. 
Each process has a PID (Process ID).
We use the arguments -e to list "every" process and -f for a "full format" output. Together they can be used as -ef. This is called standard syntax.
We use a to list processes for all users, x to list processes that aren't running in a terminal, and u for a "user-readable" output. Together can be used as aux.
These are a part of "BSD syntax".

# 2) Killing processes

```bash
hacker@processes~killing-processes:~$ ps -ef
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 05:25 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bin/dojo-init /run/dojo/bin
root           7       1  0 05:25 ?        00:00:00 /run/dojo/bin/sleep 6h
root          71       1  0 05:25 ?        00:00:00 su -c /challenge/.launcher hacker
hacker        73      71  0 05:25 ?        00:00:00 /challenge/dont_run
hacker        74      73  0 05:25 ?        00:00:00 sleep 6h
hacker        75       0  0 05:25 pts/0    00:00:00 /run/dojo/bin/ssh-entrypoint
hacker        94      75  0 05:26 pts/0    00:00:00 ps -ef

hacker@processes~killing-processes:~$ kill 73
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{QpkKyiNN1N3zfRSoQFMQAS6-aYv.dJDN4QDL4ETN0czW}
hacker@processes~killing-processes:~$ 
```
Used the kill command to kill a process. 
The PID must be used as an argument to kill a process.
The PID can be found using the ps -ef command.

# 3) Interrupting processes 
```bash
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember, 
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{IZBJZQbTxvLPWUBHWYpuqJY569-.dNDN4QDL4ETN0czW}
```
Used ctrl + c to interrupt a process.
It affects only the foreground process, making it more useful during interactive sessions.

# 4) Suspending processes
```bash
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          84      65  0 05:35 pts/0    00:00:00 bash /challenge/run
root          86      84  0 05:35 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can 
background me with Ctrl-Z or, if you're not ready to do that for whatever 
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          84      65  0 05:35 pts/0    00:00:00 bash /challenge/run
root          91      65  0 05:36 pts/0    00:00:00 bash /challenge/run
root          93      91  0 05:36 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{A6J2yNRkn6Bwd1pTGAqfocixlTX.dVDN4QDL4ETN0czW}
```
Used ctrl + z to suspend a process.
We called /challenge/run first time and suspended it so it kind of paused.
Then called it again which created another copy of it, which satisfied the conditionn given in the problem.






