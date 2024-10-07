# Sym links

A soft/symbolic link, instead, contains the original file name. When we access the symbolic link, Linux will realize that it is a symbolic link, read the original file name, and then (typically) automatically access that file

Symbolic links are created with the ln command with the -s argument

Note that the original file path comes before the link path in the command!

A symlink can be identified as such with a few methods. For example, the file command, which takes a filename and tells you what type of file it is, will recognize symlinks:

```bash
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{8ketMwalPhChw71PEghp9h2mBaH.dlTM1UDL4ETN0czW}
hacker@commands~linking-files:~$
```

