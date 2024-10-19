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



