# Untangling Users

## Becoming Root With SU
The SU command is used to switch to the root user
#### Method
- First run the SU command to switch the root, and then enter the password hack-the-planet
- Then to get the flag run cat /flag

```bash
Connected!
hacker@users~becoming-root-with-su:~$ su
Password:
su: Authentication failure
hacker@users~becoming-root-with-su:~$ su
Password:
root@users~becoming-root-with-su:/home/hacker# cat /flag
pwn.college{UTFh22eLvz4Vx6egAQHCjoSQl8E.dVTN0UDL4ETO0czW}
root@users~becoming-root-with-su:/home/hacker#
```

## Other Users With SU
The SU command can also be used to switch to other users, In this we try to switch to zardus to get the flag
#### Method
- I run the su zardus to switch user to zardus and then enter the password- dont-hack-me
- Then execute /challenge/run to get the flag

```bash
Connected!
hacker@users~other-users-with-su:~$ su zardus
Password:
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{oktxan0-ayChVAbPURjuUisc3TP.dZTN0UDL4ETO0czW}
zardus@users~other-users-with-su:/home/hacker$
```
## Cracking Passwords
In this problem we use the john command to get the password for the zardus user
#### Method
- We start by running john /challenge/shadow-leak to get the password
- The password after putting that is aardvark
- Then we run su zardus to switch zardus user profile, with aardvark password
- Then i run /challenge/run to get the flag

```bash
Connected!
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Created directory: /home/hacker/.john
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
aardvark     	(zardus)
1g 0:00:00:20 100% 2/3 0.04901g/s 285.4p/s 285.4c/s 285.4C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password:
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{EAlK3J6qE9r83ZqDaZ8-bMYy_pl.ddTN0UDL4ETO0czW}
zardus@users~cracking-passwords:/home/hacker$
```
## Using SUDO
The sudo command helps in providing the user privileges to run command that they otherwise won't be able to.

```bash
Connected!
hacker@users~using-sudo:~$ sudo cat /flag
pwn.college{sZS_VGG1agNs9s-Ni_jkoa6f9Bc.dhTN0UDL4ETO0czW}
hacker@users~using-sudo:~$
```
