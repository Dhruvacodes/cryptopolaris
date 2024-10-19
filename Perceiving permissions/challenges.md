# 1) Changing file ownership

```bash
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{AUTm_P-I4oMzRJHf7k6RUnXyRfA.dFTM2QDL4ETN0czW}
```
Here, we used the chown command to change the ownership of the /flag file.
The syntax for doing so is chown (username) (file).

# 2) Groups and files

```bash
hacker@permissions~groups-and-files:~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{0MY7s1RaFlgkLmmWhYdmcn2kOin.dFzNyUDL4ETN0czW}
```

In Linux, every file is linked to a user and a group. Users in the same group can access the file together. To allow other users in that group to access a file, you can use the `chgrp` command to change the file's group. The accessibility will depend on the permissions assigned to that group.
Here, we used the chgrp command to change the group ownership of /flag to the hacker, allowing group access.

# 3) Fun with group names

```bash
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp24516) groups=1000(grp24516)
hacker@permissions~fun-with-groups-names:~$ chgrp grp24516 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{EBWAR90Kumuy0Xuzba6y3v57Zdj.dJzNyUDL4ETN0czW}
```

Used the id command to find the groups the user is in.
Changed the group of the /flag file to the grp24516 group. 

# 4) Changing permissions

```bash
hacker@permissions~changing-permissions:~$ chmod a+r /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{ENRjwXvN_dSRa58ijSGyNNsRdVw.dNzNyUDL4ETN0czW}
```
Used the chmod function to change the permissions of a file or directory. It allows us to control who can read, write, or execute a file by specifying permissions for the owner, group, and others.
chmod MODE FILE
The mode is of format WHO+/-WHAT, where WHO is user(u)/group(g)/other(o/a) and WHAT is read(r)/write(w)/execute(x).

# 5) Executable files

```bash
hacker@permissions~executable-files:~$ chmod a+x /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{APkTSF_qNtPbFzW9z7oqQFe6Kf1.dJTM2QDL4ETN0czW}
```
Same concept as the previous question. Just made the file executable with x this time.

