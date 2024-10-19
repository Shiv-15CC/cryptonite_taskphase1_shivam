# Perceiving Permissions

## Changing File Ownership
In this module it helps us to explain about handling permissions of files
#### Method
- We need to change the owner of /flag to hacker by using chown hacker /flag
- We get the flag by cat /flag
```bash
Connected!
hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{E8SB5xC-6dbpbRtKCZOiW_9-FOc.dFTM2QDL4ETO0czW}
hacker@permissions~changing-file-ownership:~$ 
```

## Groups and Files
In this problem we see the involvement of changing the group ownership of a file using chgrp
#### Method
- Check the group id using id, there are 1000
- Change the ownership to group 1000 using chgrp 1000/flag
- Get the flag by cat /flag
```bash
                                                                  Connected!
hacker@permissions~groups-and-files:~$ id
uid=1000(hacker) gid=1000(hacker) groups=1000(hacker)
hacker@permissions~groups-and-files:~$ chgrp 1000 /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{clcDuGK0GAMB6VuiUUFGu1SNpeX.dFzNyUDL4ETO0czW}
hacker@permissions~groups-and-files:~$ 
```
## Fun With Groups Names
This is same as the previous one in this we just need to figure our the group we are in and it's id before changing ownership
#### Method
- Use id to get some information 
- The group name grp29269 seems like that is the grp, hence 1000 will be the group id
- Execute chgrp 1000 /flag to change ownership of the flag to group with id 1000
- Get the flag using cat /flag
```bash
Connected!
hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp29269) groups=1000(grp29269)
hacker@permissions~fun-with-groups-names:~$ chgrp 1000 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{4FaqmXGPpsYDik46t6DZ4tCoXlY.dJzNyUDL4ETO0czW}
hacker@permissions~fun-with-groups-names:~$ 
```

## Changing Permissions
In this problem we need to change the permission of the/flag file
#### Method
- I start by giving all users read permission using o+r /flag 
- I get the flag by cat /flag

```bash
Connected!
hacker@permissions~changing-permissions:~$ chmod o+r /flag
hacker@permissions~changing-permissions:~$ cat /flag
pwn.college{wOivGq9Qze7NBha_z1F1oj23lS4.dNzNyUDL4ETO0czW}
hacker@permissions~changing-permissions:~$ 
```

## Executable Files
This problem is an extension of the previous problem in which we need to make /challenge/run executable and then execute it to get the flag
#### Method
- I use chmod u+x /challenge/run to get the current user execute permissions 
- I then execute /challenge/run and get the flag

```bash
Connected!
hacker@permissions~executable-files:~$ chmod u+x /challenge/run
hacker@permissions~executable-files:~$ /challenge/run
Successful execution! Here is your flag:
pwn.college{gTLpJP0Pubcr23nU2BhmeImQ2u9.dJTM2QDL4ETO0czW}
hacker@permissions~executable-files:~$
```

## Permission Tweaking Practice
In this the user can cha get the permission using tools that are taught till present
#### Method


```bash

```

## Permissions Setting Practice
In this problem instead of adding or removing permissions we just set like chmod o=x /command
#### Method


```bash

```
## The SUID Bit
Some programs may be liked with SUID(set user id)Bits, which change the user to owner of the file, upon execution
#### Method

- I set a SUID ID by executing chmod u+s /challenge/get root
- I run /challenge/getroot opening 
- To get flag I run cat /flag
- 
```bash
Connected!
hacker@permissions~the-suid-bit:~$ chmod u+s /challenge/getroot
hacker@permissions~the-suid-bit:~$ /challenge/getroot
SUCCESS! You have set the suid bit on this program, and it is running as root! 
Here is your shell...
root@permissions~the-suid-bit:~# cat /flag
pwn.college{YeIPzovkVRBJuanA5kIFFUuyMdM.dNTM2QDL4ETO0czW}
root@permissions~the-suid-bit:~# 
```
