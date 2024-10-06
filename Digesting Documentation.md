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
