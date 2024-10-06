# Digesting Documentation

## Learning From Documentation

We will learn to access and read the documentation to find out alot of programs 
For this as directed i used the --giveflag argument with /challenge/challenge to get the flag
The command would be   /challenge/challenge --giveflag

    Connected!                                                                        
    hacker@man~learning-from-documentation:~$ --giveflag
    ssh-entrypoint: --giveflag: command not found
    hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
    Correct argument! Here is your flag:
    pwn.college{8rRjZJ9MdMzegJMEFg4yk-QMRfj.dRjM5QDL4ETO0czW}

## Learning Complex Usage 

In this he command themselves take up the argument 

for this we start off with /challenge/challenge --printfile/challenge/DESCRIPTION.md
then to get the flag i just used the command /challenge/challenge --printfile /flag

    Connected!                                                                        
    hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /challenge/DESCRIPTION.md
    Correct argument! Here is the /challenge/DESCRIPTION.md file:
    While using most commands is straightforward, the usage of some commands can get quite complex.
    For example, the arguments to commands like `sed` and `awk`, which we're definitely not getting into right now, are entire programs in an esoteric programming language!
    Somewhere on the spectrum between `cd` and `awk` are commands that take arguments to their arguments...
    This sounds crazy, but you've already encountered this with the `find` level in [Basic Commands](../commands).find` has a `-name` argument, and the `-name` argument itself        takes an argument specifying the name to search for.
    Many other commands are analogous.
    Here is this level's documentation for `/challenge/challenge`:
    > Welcome to the documentation for `/challenge/challenge`! This program allows you to print arbitrary files to the terminal, when given the `--printfile` argument. The            argument to the `--printfile` argument is the path of the flag to read. For example, `/challenge/challenge --printfile /challenge/DESCRIPTION.md` will print out the               description of the level!
    Given that documentation, go get the flag!
    hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
    Correct argument! Here is the /flag file:
    pwn.college{8hvE0OPErS00raSzAVGNmTgkxys.dVjM5QDL4ETO0czW}

## Reading Manuals

From this Reading Manuals we get to learn a new command which is the 'man' this is used to display the manual for any command that is given to us as an argument 
We start by using 'man challenge' 
in the manual the command '/challenge/challenge --wqusbhh 744' is given to get the flag 

    Connected!                                                                        
    man hacker@man~reading-manuals:~$ man  challenge

    CHALLENGE(1)                                                                     Challenge Commands                                                                                CHALLENGE(1)

    NAME
       /challenge/challenge - print the flag!

    SYNOPSIS
       challenge <u style="text-decoration-style:solid">OPTION</u>

    DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --wqsbhh NUM
              print the flag if NUM is 744

    AUTHOR
       Written by Zardus.

    REPORTING BUGS
       The repository for this dojo: &lt;https://github.com/pwncollege/linux-luminarium/&gt;

    SEE ALSO
       man(1) bash-builtins(7)

    pwn.college                                                                           May 2024                                                                                     CHALLENGE(1)
    hacker@man~reading-manuals:~$ /challenge/challenge --wqsbhh 744
    Correct usage! Your flag: pwn.college{wqSAsLbRhhKaHowR_AkjIpdLv7f.dRTM4QDL4ETO0czW}
 
