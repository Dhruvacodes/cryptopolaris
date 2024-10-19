# 1) Becoming root with su

```bash
hacker@users~becoming-root-with-su:~$ su
Password: 
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{0rROmi2vCLC0pq5garAL-jEqzeL.dVTN0UDL4ETN0czW}
```
Used the su command to gain root accesss.
su is a setid binary



# 2) Other users with su

```bash
hacker@users~other-users-with-su:~$ su zardus
Password: 
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{MjawbHU8S5yHjuMFPedGQn5o3iW.dZTN0UDL4ETN0czW}
```
su can be used to access another username by passing that particular username as an argument to su.

# 3) Cracking passwords

```bash

```
