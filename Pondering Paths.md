# Pondering Paths

## The Root

In this challenge I used the pwn program using its absolute path, starting with root / and directory name pwn.

      Connected!                                                                        
      hacker@paths~the-root:~$ /pwn
      BOOM!!!
      Here is your flag:
      pwn.college{EAEzIOtgCxWKGNmTKCYMEs4PE5V.dhzN5QDL4ETO0czW}

## Program and Absolute Paths

This time the absolute path was a little more nested, with the run challenge being within the challege which was within root directory.

      Connected!                                                                        
      hacker@paths~program-and-absolute-paths:~$ /challenge/run
      Correct!!!
      /challenge/run is an absolute path! Here is your flag:
      pwn.college{0-QaUYLHj6XtlP34kikYjc44osB.dVDN1QDL4ETO0czW}

## Position Thy Self 

For this one I ran /challenge/run but this time it located in a different directory called /var, then I used the cd to change the current working directory to /var then ran the /challenge/run path in it to get the key.

    Connected!                                                                        
    hacker@paths~position-thy-self:~$ /challenge/run
    Incorrect...
    You are not currently in the /usr/share/zoneinfo/posix/Asia directory.
    Please use the `cd` utility to change directory appropriately.
    hacker@paths~position-thy-self:~$ cd /usr/share/zoneinfo/posix/Asia
    hacker@paths~position-thy-self:/usr/share/zoneinfo/posix/Asia$ /challenge/run
    Correct!!!
    /challenge/run is an absolute path, invoked from the right directory!
    Here is your flag:
    pwn.college{Mhat4uHkf0_vCFYnZYXmr-o0S8T.dZDN1QDL4ETO0czW}

## Position Elsewhere 

The cd command lets us change the current working directory and then when we enter /challenge/run once it give us a working cd, then we need to change the current working directory to the one provided to us and then run /challege/run again to gain a flag.

    Connected!                                                                        
    hacker@paths~position-elsewhere:~$ /challenge/run
    Incorrect...
    You are not currently in the /usr/aarch64-linux-gnu/include/gnu directory.
    Please use the `cd` utility to change directory appropriately.
    hacker@paths~position-elsewhere:~$ cd /usr/aarch64-linux-gnu/include/gnu
    hacker@paths~position-elsewhere:/usr/aarch64-linux-gnu/include/gnu$ /challenge/run
    Correct!!!
    /challenge/run is an absolute path, invoked from the right directory!
    Here is your flag:
    pwn.college{4ausxN1LmhijvQcLCOKDa4wfnm0.ddDN1QDL4ETO0czW}

## Position Yet Elsewhere

In this first we enter the /challenge/run it shows we aren't in the current working cd, after that it will shows us the new direcoty, which we would change- cd /sys after which we run /challenge/run command which gets us the flag 

    Connected!                                                                        
    hacker@paths~position-yet-elsewhere:~$ cd /sys
    hacker@paths~position-yet-elsewhere:/sys$ /challenge/run
    Correct!!!
    /challenge/run is an absolute path, invoked from the right directory!
    Here is your flag:
    pwn.college{claILGsq2x9moJG4jRdvZPx94Gq.dhDN1QDL4ETO0czW}

## Implicit Relative Paths, from /

In this challenge, we first need to use a relative path for the file, it must start from the current working directory(cwd), From the cwd / , the relative path is /tmp/a/b/my_file is tmp/a/b/my_file, after that / is a directory in which we then run challenge/run to get the flag 

    Connected!                                                                        
    hacker@paths~implicit-relative-paths-from-:~$ /
    ssh-entrypoint: /: Is a directory
    hacker@paths~implicit-relative-paths-from-:~$ cd /
    hacker@paths~implicit-relative-paths-from-:/$ challenge/run
    Correct!!!
    challenge/run is a relative path, invoked from the right directory!
    Here is your flag:
    pwn.college{sPBeIsDd1R7KrneR7_yfGKIPJCP.dlDN1QDL4ETO0czW}

##   Explicit Relative Paths, from /

This program is same as last one in this we need to just use the explicit relative path like ./challenge/run
Then to start it we need to change the directory from /cd to / after which we run the ./challenge/run command as told in the problem 

    Connected!                                                                        
    hacker@paths~explicit-relative-paths-from-:~$ cd /
    hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
    Correct!!!
    ./challenge/run is a relative path, invoked from the right directory!
    Here is your flag:
    pwn.college{A7gruZbySL3F5gpiy4nvBXqbRYx.dBTN1QDL4ETO0czW}

## Implicit Relative Path

for this challenge we need to run the `run` command from the `/challenge` directory, use `./run` to explicitly specify that we are executing the program in the current directory. 

    Connected!                                                                        
    hacker@paths~implicit-relative-path:~$ /challenge
    ssh-entrypoint: /challenge: Is a directory
    hacker@paths~implicit-relative-path:~$ cd /challenge
    hacker@paths~implicit-relative-path:/challenge$ run
    ssh-entrypoint: run: command not found
    hacker@paths~implicit-relative-path:/challenge$ ./run
    Correct!!!
    ./run is a relative path, invoked from the right directory!
    Here is your flag:
    pwn.college{QrZczm8b3ixpeRrrl8VVJjOrV5-.dFTN1QDL4ETO0czW}

## Home Sweet Home



    Connected!                                                                        
    hacker@paths~home-sweet-home:~$ /challenge/run ~/~
    Writing the file to /home/hacker/~!
    ... and reading it back to you:
    pwn.college{Md8aNa7VMUWcfMaYve72DJL2W-L.dNzM4QDL4ETO0czW}





