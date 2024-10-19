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
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
0g 0:00:00:14 0% 2/3 0g/s 268.8p/s 268.8c/s 268.8C/s francine..me
0g 0:00:00:17 0% 2/3 0g/s 270.0p/s 270.0c/s 270.0C/s rockie..surfing
0g 0:00:00:20 1% 2/3 0g/s 271.1p/s 271.1c/s 271.1C/s ncc1701d..1022
0g 0:00:00:21 1% 2/3 0g/s 271.0p/s 271.0c/s 271.0C/s Johnson..buzz
aardvark         (zardus)
1g 0:00:00:21 100% 2/3 0.04655g/s 271.0p/s 271.0c/s 271.0C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ john --show /challenge/shadow-leak
hacker:NO PASSWORD:20000:0:99999:7:::
zardus:aardvark:20015:0:99999:7:::

2 password hashes cracked, 0 left
hacker@users~cracking-passwords:~$ su zardus
Password: 
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{85jPBaILThp74uqOeJBHa0vkfuZ.ddTN0UDL4ETN0czW}
```
Used John the ripper to get password from /challenge/shadow-leak
Used show to view the passwords.
Used su to access zardus user
Entered the shown password
Successfully run /challenge/run

