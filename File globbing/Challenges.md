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

# Matching with ? 

```bash
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{wECIEolE7IIAkRiMhkmDIuHwxkS.dJjM4QDL4ETN0czW}
hacker@globbing~matching-with-:/challenge$ 
```

# Matching with []

```bash
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{4shLUfd7lORHo0w7vnt1DVC_U2X.dNjM4QDL4ETN0czW}
hacker@globbing~matching-with-:/challenge/files$ 
```

# Matching paths with []

```bash
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{4DcLwp7gLOQr8GifbsZmS0o4Y-s.dRjM4QDL4ETN0czW}
hacker@globbing~matching-paths-with-:~$ 
```
# Mixing globs

```bash
hacker@globbing~mixing-globs:~$ cd /challenge/files
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{I2_HzV8v4gpw3aE4GB9gPY-kSs-.dVjM4QDL4ETN0czW}
hacker@globbing~mixing-globs:/challenge/files$ 
```
# Exclusionary Globbing

```bash
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [!pwn]*
You got it! Here is your flag!
pwn.college{sf1MhC-D8-885IHKEwKfuC3Slr-.dZjM4QDL4ETN0czW}
hacker@globbing~exclusionary-globbing:/challenge/files$ 
```
