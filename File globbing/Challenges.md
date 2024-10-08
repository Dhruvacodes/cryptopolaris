# Matching with *

```bash
Connected!                                                                        
This challenge resets your working directory to /home/hacker unless you change 
directory properly...
hacker@globbing~matching-with-:~$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{MEIKR5IJ3yn68LTuvNlFwN0Pjh8.dFjM4QDL4ETN0czW}
hacker@globbing~matching-with-:/challenge$ 
```
The shell sees a * in arguments as a "wildcard."
It tries to find files matching the pattern to replace the argument.
If no files match, the shell doesn't change the argument.
The * can match any part of a filename, but not the / or a dot (.) at the start.
Here we moved to the challenge directory using /ch*.

# Matching with ? 

```bash
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{wECIEolE7IIAkRiMhkmDIuHwxkS.dJjM4QDL4ETN0czW}
hacker@globbing~matching-with-:/challenge$ 
```
The shell sees a ? in arguments as a "wildcard" too.
The ? can match any part of a filename, but not the / or a dot (.) at the start.
The only difference is that it matches only one character.

# Matching with []

```bash
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{4shLUfd7lORHo0w7vnt1DVC_U2X.dNjM4QDL4ETN0czW}
hacker@globbing~matching-with-:/challenge/files$ 
```
[] is a limited form of ? where we provide a subset to potential characters to search for. For example, here [bash] will search for files with b, a, s, or h in the ending.

# Matching paths with []

```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{4DcLwp7gLOQr8GifbsZmS0o4Y-s.dRjM4QDL4ETN0czW}
hacker@globbing~matching-paths-with-:~$ 
```
We can use [] to expand paths as well.

# Mixing globs

```bash
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{I2_HzV8v4gpw3aE4GB9gPY-kSs-.dVjM4QDL4ETN0czW}
hacker@globbing~mixing-globs:/challenge/files$ 
```
First, we moved to the /challenges/files directory using cd as mentioned in the question
Then we used [cep]* to find a file that starts with c,e, or p and used * to expand our search to  "challenging", "educational", and "pwning".

# Exclusionary Globbing

```bash
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{sf1MhC-D8-885IHKEwKfuC3Slr-.dZjM4QDL4ETN0czW}
hacker@globbing~exclusionary-globbing:/challenge/files$ 
```
If we use ! or ^ inside a [], it will look for characters that are not listed inside it.
