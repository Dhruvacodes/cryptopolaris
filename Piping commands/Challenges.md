# 1.) Redirecting Output

```bash
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your 
flag:
pwn.college{8HLCEb_5jprH-GasMJVc0VrzN-0.dRjN1QDL4ETN0czW}
```
we can use the > command to redirect the output of a command to another file.
Here I redirected PWN to COLLEGE which would have printed PWN when I would have called for COLLEGE.

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
We verified that > can be used to redirect the content of files to other files as well. 
used > to redirect /challenge/run to myflag.
Then, I used the cat command to read myflag.
easy!

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
We can use >> to append a file. 
In this case, I appended stdout to the /home/hacker/the-flag file 
Then, I used the cat command to read into it.

# 4.) Redirecting errors

```bash
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{oFGWMtBD5EmHGunMyZI8LvmShTW.ddjN1QDL4ETN0czW}

```
we can use a file descriptor before > so that we can specify whether it's an output error or input. By default,> means 1>, which is the standard output. 0 is input, and 2 is output.
We can do multiple redirections in one go. Here, I first redirected the output of /challenge/run to myflag, and the error in the file was sent to instructions.

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
We can use < to redirect input into programs.
Here we first redirected COLLEGE into PWN and then redirected it's input into /challenge/run.

# 6.) Grepping Stored Results

```bash
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep pwn.college{  /tmp/data.txt
pwn.college{YA7QgmTCyJTJunVT5YrnKT5wuiu.dhTM4QDL4ETN0czW}
hacker@piping~grepping-stored-results:~$ 

```
Redirected the output of /challenge/run to /tmp/data.txt
The used the grep command to find the key from /tmp/data.txt. WE KNOW THAT THE KEY STARTS WITH pwn.college{ .

# 7.) Grepping live output

```bash
hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.college{
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{Qz88QvSvJALOONzPm_Vrpixand8.dlTM4QDL4ETN0czW}
hacker@piping~grepping-live-output:~$ 

```
Use the | (pipe) operator to avoid saving results to a file, making things simpler.
This connects the output of the command on the left directly into the input of the command on the right. 

# 8.) Grepping errors

```bash
Connected!                                                                        
hacker@piping~grepping-errors:~$ /challenge/run 2>&1 | grep pwn.college{
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{cdEOJYa8_cNquYUzx3_85VFh3Dk.dVDM5QDL4ETN0czW}
hacker@piping~grepping-errors:~$ 

```
We redirected standard error to standard output using >& .
Then we piped both error and output using |
Finally we used grep to find the key that always starts with pwn.college{


# 9.) Duplicating piped data with tee

```bash
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn |tee output | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code 
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the 
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat output
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "UBZZdl2X"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret "UBZZdl2X"
Processing...
You must pipe the output of /challenge/pwn into /challenge/college (or 'tee' 
for debugging).
hacker@piping~duplicating-piped-data-with-tee:~$  /challenge/pwn --secret "UBZZdl2X" | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{UBZZdl2XKWt9zIZMtPGzJFXdJBZ.dFjM5QDL4ETN0czW}
hacker@piping~duplicating-piped-data-with-tee:~$ 

```

# 10.) Writing to multiple programs

```bash
Connected!                                                                        
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >( /challenge/the ) | /challenge/planet
Congratulations, you have duplicated data into the input of two programs! Here 
is your flag:
pwn.college{4iUxD7eZ1U-uYAGrIXxAJHn1Ene.dBDO0UDL4ETN0czW}
hacker@piping~writing-to-multiple-programs:~$ 

```

# 11.) Split piping stderr and stdout

```bash
pwn.college{IhoqKWRTATKD7YJYCz3bnYW9dWe.dFDNwYDL4ETN0czW}

```
