# Pondering PATH

## The PATH Variable
The PATH variable is a system setting that tells us where to look for programs to run. In this case, we change the PATH so that it can't find the "rm" command.

#### Method
- I set the PATH variable to nothing using PATH=" "
- Then I run /challenge/run as the rm command should not be found anywhere 
- Then I get the flag

```bash
Connected!
hacker@path~the-path-variable:~$ PATH=""
hacker@path~the-path-variable:~$ /challenge/run
Trying to remove /flag...
/challenge/run: line 4: rm: No such file or directory
The flag is still there! I might as well give it to you!
pwn.college{AdSQTV0op4R9UdaLm-QA_fCnUEl.dZzNwUDL4ETO0czW}
hacker@path~the-path-variable:~$
```

## Setting PATH
This problem introduces a new command to PATH that is win

#### Method
- I start by executing PATH=$PATH:/challenge/more_commands/ appending a new directory to the old PATH
- After the PATH is updated run /challenge/run to get the flag

```bash
Connected!
hacker@path~setting-path:~$ ls /challenge/more_commands/
win
hacker@path~setting-path:~$ export PATH=$PATH:/challenge/more_commands/
hacker@path~setting-path:~$ /challenge/run
Invoking 'win'....
Congratulations! You properly set the flag and 'win' has launched!
pwn.college{syFZOoCdSrdHG0GHHeDVojoPxpp.dVzNyUDL4ETO0czW}
hacker@path~setting-path:~$
```

## Adding Commands

## Hijacking Commands
