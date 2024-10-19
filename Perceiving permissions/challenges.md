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

# 6) Permissison tweaking practice

```bash
chmod o-r /challenge/pwn
chmod g-r /challenge/pwn
chmod g+wx /challenge/pwn
chmod o+x /challenge/pwn
chmod a-rw g-w /challenge/pwn
chmod go+r /challenge/pwn
chmod a-rwx /challenge/pwn
chmod a+x /challenge/pwn
hacker@permissions~permission-tweaking-practice:~$ chmod a+r /flag
hacker@permissions~permission-tweaking-practice:~$ cat /flag
pwn.college{kcDPuYrKNCsQon1TlrZXJ1yCoTx.dBTM2QDL4ETN0czW}
```
Played a game with 8 rounds to get the flag file. 
Made the flag file readable and then used cat to read into it.

# 7) Permissions setting practice

```bash
chmod g=rw,o=wx /challenge/pwn
chmod u=w,g=wx,o=w /challenge/pwn
chmod g=-,o=wx /challenge/pwn
chmod u=-,g=r,o=rwx /challenge/pwn
chmod u=rwx,g=-,o=rx /challenge/pwn
chmod u=rw,g=w,o=wx /challenge/pwn
chmod u=-,g=wx,o=rw /challenge/pwn
chmod u=r,g=x,o=wx /challenge/pwn
hacker@permissions~permissions-setting-practice:~$ chmod a+r /flag
hacker@permissions~permissions-setting-practice:~$ cat /flag
pwn.college{Ao1NVZCg-jpAr3lEqIF8BpW_dIA.dNTM5QDL4ETN0czW}
```
Solved the same game but with = and - commands this time.
= can be used to set the permissions simply.






