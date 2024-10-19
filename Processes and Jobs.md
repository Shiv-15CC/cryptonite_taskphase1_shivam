# Processes and Jobs

## Listing Processes
In this module it tells us about the processes, which are the operations that occur in the background and are the essential part of the system

### Method
- To start with use px aux to display the processes, to get the flag ps aux,
- After finding the right process, use /challenge/
```bash
hacker@processes~listing-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.0   1056   640 ?        Ss   12:41   0:00 /sbin/docker-init -- /nix/var/nix/profiles/default/bin/dojo-init /run/dojo/bin/sleep 6h
root           7  0.0  0.0   5052  2560 ?        S    12:41   0:00 /run/dojo/bin/sleep 6h
root          69  0.0  0.0   4132  2880 ?        S    12:41   0:00 /challenge/3138-run-25095
root          73  0.0  0.0   2744  1600 ?        S    12:41   0:00 sleep 6h
hacker        74  0.0  0.0   5240  3840 pts/0    Ss   12:41   0:00 /run/dojo/bin/ssh-entrypoint
hacker        94  0.0  0.0   7868  3200 pts/0    R+   12:44   0:00 ps aux
hacker@processes~listing-processes:~$ /challenge/3138-run-25095
Yahaha, you found me! Here is your flag:
pwn.college{sMHestIK03uKTZwVjp0Tw-hF529.dhzM4QDL4ETO0czW}
Now I will sleep for a while (so that you could find me with 'ps').
```

## Killing Processes
This problem deals with terminating processes using the kill command
### Method
To get the flag we start off with 
-Use ps aux to fi d the PID of the /challenge/dont_run command
-then use kill /challenge/dont_run to kill that process
-then to get the flag use /challenge/run
```bash
Connected!                                                                        
hacker@processes~killing-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.4  0.0   1056   640 ?        Ss   12:45   0:00 /sbin/docker-
root           7  0.0  0.0   5052  2240 ?        S    12:45   0:00 /run/dojo/bin
root          71  0.0  0.0   4732  2880 ?        S    12:45   0:00 su -c /challe
hacker        73  0.0  0.0   4976  3200 ?        Ss   12:45   0:00 /challenge/do
hacker        74  0.0  0.0   5052  2560 ?        S    12:45   0:00 sleep 6h
hacker        75  0.4  0.0   5240  3840 pts/0    Ss   12:45   0:00 /run/dojo/bin
hacker        92  0.0  0.0   7868  3200 pts/0    R+   12:45   0:00 ps aux
hacker@processes~killing-processes:~$ kill 74
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{U01rMI3TI5xBYy7gOlJNxvdzLX4.dJDN4QDL4ETO0czW}
```

## Interrupting Processes
Interrupting is another way to kill the process, this is mostly done by codes like Ctrl+C
### Method
- Start with /challenge/run
- I would not get the flag until I use the Ctrl+C command to interrupt the program
```bash
Connected!                                                                        
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember, 
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{8-8XugBeAKHLQpXjt0meSPQPjLf.dNDN4QDL4ETO0czW}
hacker@processes~interrupting-processes:~$ 
```

## Suspending Processes
In this module we suspend the processes, It is same like the previous one in this we need to run Ctrl+Z 
### Method
- To start off with run /challenge/run we get a prompt to suspend it 
- to suspend the process using Ctrl+Z
- Then run /challenge/run again as told to get 2 instances of running
```bash
                                                                                                                                                                Connected!
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          82      65  0 12:51 pts/0    00:00:00 bash /challenge/run
root          84      82  0 12:51 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can 
background me with Ctrl-Z or, if you're not ready to do that for whatever 
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in 
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root          82      65  0 12:51 pts/0    00:00:00 bash /challenge/run
root          89      65  0 12:51 pts/0    00:00:00 bash /challenge/run
root          91      89  0 12:51 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{wPoi6zBtoIkAKwgku32MbbuzEiw.dVDN4QDL4ETO0czW}
hacker@processes~suspending-processes:~$ 
```

## Resuming Processes
In this process we can resume then with fg which means foreground command
### Method
- To start with use /challenge/run and get the prompted to suspend the process 
- To resume it by executing fg, after which we get the flag
```bash
Connected!                                                                        
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with 
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{Uf96As7PCcCHBGErC2DEdD0V33e.dZDN4QDL4ETO0czW}
```

## Backgrounding Processes
As we learnt In the previous one how to resume the foreground processes, in this we will learn how to resume the Background processes also by bg command
### Method
- Start with /challenge/run and then suspend by Ctrl+Z
- Then resume the Background process by bg command
- Then to start a new instance type out /challenge/run, now I have 2 processes, thereafter getting the flag
```bash
                                                                                                                                                                Connected!
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root          82 S+   bash /challenge/run
root          84 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the 
background, and then launch a new version of me! You can background me with 
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to 
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &



Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out.
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and 
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root          82 S    bash /challenge/run
root          92 S    sleep 6h
root          93 S+   bash /challenge/run
root          95 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{oY3sENFxU2dTYzS70Nd9ejHG2DK.ddDN4QDL4ETO0czW}
hacker@processes~backgrounding-processes:~$ 
```

## Foregrounding Processes
This is a combination to both the foreground and Background process
### Method
- We Start by using /challenge/run, and the suspend it
- Then I Background the process by bg
- After which we foreground it by fg, getting the flag
```bash
Connected!                                                                        
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the 
background, and *then* foreground it without re-suspending it! You can 
background me with Ctrl-Z (and resume me in the background with 'bg') or, if 
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg
[1]+ /challenge/run &



hacker@processes~foregrounding-processes:~$ Yay, I'm now running the background! Because of that, this text will probably 
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times 
to scroll this text out. After that, resume me into the foreground with 'fg'; 
I'll wait.
fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{Qp0X85cjV4rewHW6UuhS8NvWjSH.dhDN4QDL4ETO0czW}
hacker@processes~foregrounding-processes:~$ 
```

## Starting Background Processes
Now we can background the processes straight away by appending & after the command
### Method
Run the /challenge/run & to start /challenge/run in the background
```bash
Connected!                                                                        
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 82



hacker@processes~starting-backgrounded-processes:~$ Yay, you started me in the background! Because of that, this text will probably 
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{YQlW8REg7vydzJlUo7W7ma4tQ9N.dlDN4QDL4ETO0czW}
```

## Process Exit Codes
```bash
Connected!                                                                        
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
130
hacker@processes~process-exit-codes:~$ /challenge/submit-code 130
CORRECT! Here is your flag:
pwn.college{05Mbr3A9Q5TccKF9sfuzVi1mJgV.dljN4UDL4ETO0czW}
hacker@processes~process-exit-codes:~$ 
```

