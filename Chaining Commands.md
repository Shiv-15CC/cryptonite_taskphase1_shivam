# Chaining Commands

## Chaining with Semicolons
In this problem they tell us about the use of changing command in which when we get a complex command so to make is easily understandable we use the semicolon

#### Method
- We need to chain /challenge/pwn and /challenge/college as /challenge/pwn;/challenge/college

```bash
Connected!
hacker@chaining~chaining-with-semicolons:~$ /challenge/pwn;/challenge/college
Yes! You chained /challenge/pwn and /challenge/college! Here is your flag:
pwn.college{QW9fG6wRT9Z90Zpo3VvrvuVi02m.dVTN4QDL4ETO0czW}
hacker@chaining~chaining-with-semicolons:~$
```

## Your First Shell Script
To chain it directly we also have the shell script

#### Method
- First we need to create x.sh file with the help of nano y.sh
- Then use #!/bin/bash to specify the shell script 
- Then we write /challenge/pwn:/challenge/college changing these two commands 
- Then I exit and run the script bash y.sh

```bash
Connected!                                                                        
hacker@chaining~your-first-shell-script:~$ nano y.sh
hacker@chaining~your-first-shell-script:~$ bash y.sh
Great job, you've written your first shell script! Here is the flag:
pwn.college{oldUIwzzG24G1J7Elz2QaFc8aMD.dFzN4QDL4ETO0czW}
hacker@chaining~your-first-shell-script:~$
```

## Redirecting Script Output
This problem is somewhat similar to pervious one, in this we need to redirect the script output to /challenge/solve

#### Method
- We start off to make script using nano script.sh
- The script is same as the last one /challenge/pwn;/challenge/college
- Then we pipe the output using bash script.sh | /challenge/solve and pipe it into /challenge/solve

```bash
Connected!
hacker@chaining~redirecting-script-output:~$ nano script.sh
hacker@chaining~redirecting-script-output:~$ bash script.sh | /challenge/solve
Correct! Here is your flag:
pwn.college{89TteM5XySN-SQug4fP-8POjofj.dhTM5QDL4ETO0czW}
hacker@chaining~redirecting-script-output:~$
```

## Executable Shell Scripts
In this problem we find a way to run a script instead of using the bash command

#### Method
- First I use nano script.sh to make the script as per the details of the problem and then execute /challenge/solve
- Then I give the script permissions to execute using chmod u=rwx,g=rwx,o=rwx script.sh
- Then run the script using it's absolute path /home/hacker/script.sh

```bash
Connected!
hacker@chaining~executable-shell-scripts:~$ nano script.sh
hacker@chaining~executable-shell-scripts:~$ chmod u=rwx,g=rwx,o=rwx script.sh
hacker@chaining~executable-shell-scripts:~$ nano script.sh
hacker@chaining~executable-shell-scripts:~$ /home/hacker/script.sh
Congratulations on your shell script execution! Your flag:
pwn.college{UwpGo6FLLWEWqtu9zuKWboToGpK.dRzNyUDL4ETO0czW}
hacker@chaining~executable-shell-scripts:~$
```
