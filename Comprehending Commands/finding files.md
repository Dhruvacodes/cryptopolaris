# Finding files

```bash
hacker@commands~finding-files:~$ find / -name flag
find: ‘/tmp/tmp.MiOQGWw5Zc’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
/usr/local/share/radare2/5.9.5/flag
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/mysql-files’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/mysql’: Permission denied
find: ‘/var/lib/mysql-keyring’: Permission denied
find: ‘/var/lib/php/sessions’: Permission denied
find: ‘/var/log/private’: Permission denied
find: ‘/var/log/apache2’: Permission denied
find: ‘/var/log/mysql’: Permission denied
find: ‘/run/mysqld’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/root’: Permission denied
/opt/ghidra/Ghidra/Features/Python/data/jython-2.7.3/Lib/lib2to3/flag
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
/opt/radare2/libr/flag
find: ‘/proc/tty/driver’: Permission denied
find: ‘/proc/1/task/1/fd’: Permission denied
find: ‘/proc/1/task/1/fdinfo’: Permission denied
find: ‘/proc/1/task/1/ns’: Permission denied
find: ‘/proc/1/fd’: Permission denied
find: ‘/proc/1/map_files’: Permission denied
find: ‘/proc/1/fdinfo’: Permission denied
find: ‘/proc/1/ns’: Permission denied
find: ‘/proc/7/task/7/fd’: Permission denied
find: ‘/proc/7/task/7/fdinfo’: Permission denied
find: ‘/proc/7/task/7/ns’: Permission denied
find: ‘/proc/7/fd’: Permission denied
find: ‘/proc/7/map_files’: Permission denied
find: ‘/proc/7/fdinfo’: Permission denied
find: ‘/proc/7/ns’: Permission denied
/nix/store/1yagn5s8sf7kcs2hkccgf8d0wxlrv5sz-radare2-5.9.0/share/radare2/5.9.0/flag
/nix/store/pmvk2bk4p550w182rjfm529kfqddnvh3-python3.11-pwntools-4.12.0/lib/python3.11/site-packages/pwnlib/flag
hacker@commands~finding-files:~$ ls -a /usr/local/lib/python3.8/dist-packages/pwnlib/flag
.  ..  __init__.py  __pycache__  flag.py
hacker@commands~finding-files:~$ ls -a /usr/local/share/radare2/5.9.5/flag
.  ..  tags.r2
hacker@commands~finding-files:~$ ls -a /opt/ghidra/Ghidra/Features/Python/data/jython-2.7.3/Lib/lib2to3/flag
/opt/ghidra/Ghidra/Features/Python/data/jython-2.7.3/Lib/lib2to3/flag
hacker@commands~finding-files:~$ ls -a /opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
.  ..  __init__.py  __pycache__  flag.py
hacker@commands~finding-files:~$ ls -a /opt/radare2/libr/flag
.  ..  Makefile  d  flag.c  flag.d  flag.o  libr_flag.so  meson.build  tags.c  tags.d  tags.o  zones.c  zones.d  zones.o
hacker@commands~finding-files:~$ ls -a /nix/store/1yagn5s8sf7kcs2hkccgf8d0wxlrv5sz-radare2-5.9.0/share/radare2/5.9.0/flag
.  ..  tags.r2
hacker@commands~finding-files:~$ ls -a /nix/store/pmvk2bk4p550w182rjfm529kfqddnvh3-python3.11-pwntools-4.12.0/lib/python3.11/site-packages/pwnlib/flag
.  ..  __init__.py  __pycache__  flag.py
hacker@commands~finding-files:~$ cd /opt
hacker@commands~finding-files:/opt$ cd/opt/radare2/libr/flag
ssh-entrypoint: cd/opt/radare2/libr/flag: No such file or directory
hacker@commands~finding-files:/opt$ ls -a
.   aflplusplus      binaryninja  capstone  ghidra  kropr    linux    pwn.college  radare2  splitmind  virtiofsd
..  angr-management  busybox      gef       ida     libslub  pt-dump  pwndbg       rappel   tcpdump
hacker@commands~finding-files:/opt$ cd /usr/local/lib/python3.8/dist-packages/pwnlib/flag
hacker@commands~finding-files:/usr/local/lib/python3.8/dist-packages/pwnlib/flag$ ls -a
.  ..  __init__.py  __pycache__  flag.py
hacker@commands~finding-files:/usr/local/lib/python3.8/dist-packages/pwnlib/flag$ cd /usr/local/share/radare2/5.9.5/flag
hacker@commands~finding-files:/usr/local/share/radare2/5.9.5/flag$ ls -a
.  ..  tags.r2
hacker@commands~finding-files:/usr/local/share/radare2/5.9.5/flag$ cd /nix/store/pmvk2bk4p550w182rjfm529kfqddnvh3-python3.11-pwntools-4.12.0/lib/python3.11/site-packages/pwnlib/flag
hacker@commands~finding-files:/nix/store/pmvk2bk4p550w182rjfm529kfqddnvh3-python3.11-pwntools-4.12.0/lib/python3.11/site-packages/pwnlib/flag$ ls -a
.  ..  __init__.py  __pycache__  flag.py
hacker@commands~finding-files:/nix/store/pmvk2bk4p550w182rjfm529kfqddnvh3-python3.11-pwntools-4.12.0/lib/python3.11/site-packages/pwnlib/flag$ cd /nix/store/1yagn5s8sf7kcs2hkccgf8d0wxlrv5sz-radare2-5.9.0/share/radare2/5.9.0/flag
hacker@commands~finding-files:/nix/store/1yagn5s8sf7kcs2hkccgf8d0wxlrv5sz-radare2-5.9.0/share/radare2/5.9.0/flag$ ls -a
.  ..  tags.r2
hacker@commands~finding-files:/nix/store/1yagn5s8sf7kcs2hkccgf8d0wxlrv5sz-radare2-5.9.0/share/radare2/5.9.0/flag$ cd /opt/radare2/libr/flag
hacker@commands~finding-files:/opt/radare2/libr/flag$ ls -a
.  ..  Makefile  d  flag.c  flag.d  flag.o  libr_flag.so  meson.build  tags.c  tags.d  tags.o  zones.c  zones.d  zones.o
hacker@commands~finding-files:/opt/radare2/libr/flag$ cd Makefile
ssh-entrypoint: cd: Makefile: Not a directory
hacker@commands~finding-files:/opt/radare2/libr/flag$ cat Makefile
include ../config.mk

NAME=r_flag
R2DEPS=r_util
OBJS=flag.o zones.o tags.o

include ../rules.mk
hacker@commands~finding-files:/opt/radare2/libr/flag$ find -name flag
hacker@commands~finding-files:/opt/radare2/libr/flag$ cd /opt/radare2/libr/flag
hacker@commands~finding-files:/opt/radare2/libr/flag$ find -name flag
hacker@commands~finding-files:/opt/radare2/libr/flag$ cd /opt
hacker@commands~finding-files:/opt$ find -name flag
./ghidra/Ghidra/Features/Python/data/jython-2.7.3/Lib/lib2to3/flag
./pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
./radare2/libr/flag
hacker@commands~finding-files:/opt$ cat ./ghidra/Ghidra/Features/Python/data/jython-2.7.3/Lib/lib2to3/flag
pwn.college{svMhqtRfPvg0_rpw0weiz8WyC7g.dJzM4QDL4ETN0czW}hacker@commands~finding-files:/opt$ 

```

Keep on using find until flag is obtained
