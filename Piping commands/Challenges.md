# 1.) Riderecting Output

```bash
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your 
flag:
pwn.college{8HLCEb_5jprH-GasMJVc0VrzN-0.dRjN1QDL4ETN0czW}
```

# 2.) Ridirecting More Output 

```bash
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{0OqiVi5TnHqg92SyAWlB5upi7Dt.dVjN1QDL4ETN0czW}
```
# 3.) Appending output 

```bash
hacker@piping~appending-output:~$ echo stdout >> /home/hacker/the-flag
hacker@piping~appending-output:~$ cat /home/hacker/the-flag
 | 
\|/ This is the first half:
 v 
pwn.college{Y1mK_XdQy8DSfSxtP0_x4qw3H6D.ddDM5QDL4ETN0czW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>) 
rather than *append* mode (>>), and so the write of the second half to stdout 
overwrote the initial write of the first half directly to the file. Try append 
mode!
stdout
```

# 4.) Redirecting errors

```bash
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{oFGWMtBD5EmHGunMyZI8LvmShTW.ddjN1QDL4ETN0czW}

```
# 5.) Redirecting input

```bash
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read 
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{A9OGIR7RKnkZqxvbCKw43ZwLt7l.dBzN1QDL4ETN0czW}
hacker@piping~redirecting-input:~$ 
```
