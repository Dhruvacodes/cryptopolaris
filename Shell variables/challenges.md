# 1) Printing variables

```bash
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{oh6d_t_G3vIKCjN8hhwZ9PcjgLI.ddTN1QDL4ETN0czW}
hacker@variables~printing-variables:~$ 
```
Here, we used the echo command to print the given argument.

We can also print variables in the format echo $<VARIABLE>.

# 2) Setting variables 

```bash
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{8QXquuJGbFF6Y709Jm8RuRv2M5n.dlTN1QDL4ETN0czW}
```
Here, we assigned values to variables.

The format is VARIABLE=VALUE.

We must be careful not to put spaces between the variable, value and space.

# 3) Multi word variables

```bash
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{cTcECsdizmbQyySd_HC9TekgPvj.dBjN1QDL4ETN0czW}
```
To assign a value with space to a variable VAR="VALUE VALUE" formnat should be used.

If we don't use " ", the shell interprets the second value as a command.

# 4) Exporting variables.

```bash
Connected!                                                                        
hacker@variables~exporting-variables:~$ PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ export PWN
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{o5o6getz3PyCSPDSgp-QI61M9us.dJjN1QDL4ETN0czW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$
```
A variable set in a shell is local to that particular shell, and thus, to inherit them in other shell processes, we can use the export command. When you export your variables, they are passed into the environment variables of child processes.

# 5) Printing exported variables 

```bash
Connected!                                                                        
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
DOJO_AUTH_TOKEN=7abf079b78b7111c727ac9c46db84260366422965730fe442c0d31ea7e68ccd5
HOME=/home/hacker
LANG=C.UTF-8
LS_COLORS=rs=0:di=01;34:ln=01;36:mh=00:pi=40;33:so=01;35:do=01;35:bd=40;33;01:cd=40;33;01:or=40;31;01:mi=00:su=37;41:sg=30;43:ca=00:tw=30;42:ow=34;42:st=37;44:ex=01;32:*.7z=01;31:*.ace=01;31:*.alz=01;31:*.apk=01;31:*.arc=01;31:*.arj=01;31:*.bz=01;31:*.bz2=01;31:*.cab=01;31:*.cpio=01;31:*.crate=01;31:*.deb=01;31:*.drpm=01;31:*.dwm=01;31:*.dz=01;31:*.ear=01;31:*.egg=01;31:*.esd=01;31:*.gz=01;31:*.jar=01;31:*.lha=01;31:*.lrz=01;31:*.lz=01;31:*.lz4=01;31:*.lzh=01;31:*.lzma=01;31:*.lzo=01;31:*.pyz=01;31:*.rar=01;31:*.rpm=01;31:*.rz=01;31:*.sar=01;31:*.swm=01;31:*.t7z=01;31:*.tar=01;31:*.taz=01;31:*.tbz=01;31:*.tbz2=01;31:*.tgz=01;31:*.tlz=01;31:*.txz=01;31:*.tz=01;31:*.tzo=01;31:*.tzst=01;31:*.udeb=01;31:*.war=01;31:*.whl=01;31:*.wim=01;31:*.xz=01;31:*.z=01;31:*.zip=01;31:*.zoo=01;31:*.zst=01;31:*.avif=01;35:*.jpg=01;35:*.jpeg=01;35:*.mjpg=01;35:*.mjpeg=01;35:*.gif=01;35:*.bmp=01;35:*.pbm=01;35:*.pgm=01;35:*.ppm=01;35:*.tga=01;35:*.xbm=01;35:*.xpm=01;35:*.tif=01;35:*.tiff=01;35:*.png=01;35:*.svg=01;35:*.svgz=01;35:*.mng=01;35:*.pcx=01;35:*.mov=01;35:*.mpg=01;35:*.mpeg=01;35:*.m2v=01;35:*.mkv=01;35:*.webm=01;35:*.webp=01;35:*.ogm=01;35:*.mp4=01;35:*.m4v=01;35:*.mp4v=01;35:*.vob=01;35:*.qt=01;35:*.nuv=01;35:*.wmv=01;35:*.asf=01;35:*.rm=01;35:*.rmvb=01;35:*.flc=01;35:*.avi=01;35:*.fli=01;35:*.flv=01;35:*.gl=01;35:*.dl=01;35:*.xcf=01;35:*.xwd=01;35:*.yuv=01;35:*.cgm=01;35:*.emf=01;35:*.ogv=01;35:*.ogx=01;35:*.aac=00;36:*.au=00;36:*.flac=00;36:*.m4a=00;36:*.mid=00;36:*.midi=00;36:*.mka=00;36:*.mp3=00;36:*.mpc=00;36:*.ogg=00;36:*.ra=00;36:*.wav=00;36:*.oga=00;36:*.opus=00;36:*.spx=00;36:*.xspf=00;36:*~=00;90:*#=00;90:*.bak=00;90:*.crdownload=00;90:*.dpkg-dist=00;90:*.dpkg-new=00;90:*.dpkg-old=00;90:*.dpkg-tmp=00;90:*.old=00;90:*.orig=00;90:*.part=00;90:*.rej=00;90:*.rpmnew=00;90:*.rpmorig=00;90:*.rpmsave=00;90:*.swp=00;90:*.tmp=00;90:*.ucf-dist=00;90:*.ucf-new=00;90:*.ucf-old=00;90:
FLAG=pwn.college{8L1bB71-sQ2K2l83yJEIn95peBT.dhTN1QDL4ETN0czW}
LESSCLOSE=/usr/bin/lesspipe %s %s
TERM=xterm
LESSOPEN=| /usr/bin/lesspipe %s
SHLVL=1
LC_CTYPE=C.UTF-8
PATH=/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
_=/run/workspace/bin/env
```
We can use the env command to print every exported variable value.

# 6) Storing command output

```bash
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ echo "$PWN"
pwn.college{cz85u3OfG2Ffe3qqjzXU9qSyBjv.dVzN0UDL4ETN0czW}
```
We learnt how to store the output of a command into a variable. 
Here, we used the first command, i.e. PWN=$(/challenge/run), to store the output of /challenge/run in the variable PWN.
Then, we used the second command, i.e. echo "$PWN" to read the flag stored in the variable PWN.
The format for storing the output is VAR=$(OUTPUT COMMAND)
' ' can be used in place of $() , but it is not reccomended. 

# 7) Reading Input

```bash
hacker@variables~reading-input:~$ read PWN
COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{YIHD4LD2TMqMY5hHfjS7cwFc3fB.dhzN1QDL4ETN0czW}
```
The read builtin can be used to take input from the user and store it in a variable.
Here, we took the input from the user in the PWN variable and then assigned the value COLLEGE to it.

# 8) Reading files

```bash
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{QJQoFrDtJ9mHyZE6qpS9gnXLRU3.dBjM4QDL4ETN0czW}
```
Here, we eliminated using the cat command.
We redirected the standard output of /challenge/read_me into the standard input of read PWN. 
So when the shell reads PWN, it will read the value from /challenge/run, which was redirected into the PWN variable.


