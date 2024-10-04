# Implicit relative path 


```bash
Connected!
hacker@paths~implicit-relative-path:~$ cd /
hacker@paths~implicit-relative-path:/$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{8B3lYU8n2qOShKZo0U3TPsnxtbZ.dFTN1QDL4ETN0czW}
hacker@paths~implicit-relative-path:/challenge$ 
```
Used ./to launch run in order to avoid a safety feature of linux regarding naked path. 

It avoids searching naked path because it may lead to them having the same name as core system utilities.

