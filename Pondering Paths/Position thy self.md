# Position thy self

cd ( change directory ) command. This is used to navigate around dictionaries

'Bash' is something that is used to run applications that are installed within a system

It did not show the directory until the first time it went wrong.



```bash

hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/build-essential directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /usr/share/build-essential
hacker@paths~position-thy-self:/usr/share/build-essential$ cd /challenge/run
ssh-entrypoint: cd: /challenge/run: Not a directory
hacker@paths~position-thy-self:/usr/share/build-essential$ cd /usr/share/build-essential
hacker@paths~position-thy-self:/usr/share/build-essential$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{4H6qUqp9mDE8YBG_2UvdN_0YODE.dZDN1QDL4ETN0czW}
hacker@paths~position-thy-self:/usr/share/build-essential$ 

'''

