# 1) Chaining with semicolons

```bash
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn ; /challenge/college
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{o30XpG9EZIqxwjxsg-FasVFy6mQ.dVTN4QDL4ETN0czW}
```
Used the ; to chain two commands together.
The shell will execute the first command and then move to the next command that comes after the semicolon.

# 2) Your first shell script

```bash
hacker@chaining~your-first-shell-script:~$ echo /challenge/pwn > x.sh
hacker@chaining~your-first-shell-script:~$ echo /challenge/college >> x.sh
hacker@chaining~your-first-shell-script:~$ bash x.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{MAtNnn0Mw1N1FoMPTgNt_G_qoSu.dFzN4QDL4ETN0czW}
```
Redirected output of /challenge/pwn to x.sh
Appended output of /challenge/college to x.sh
Invoked the script using bash to get the flag.
