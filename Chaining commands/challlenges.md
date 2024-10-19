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
