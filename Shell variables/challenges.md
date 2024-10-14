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



