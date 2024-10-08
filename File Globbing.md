# File Globbing

## Matching with *

In this problem we get to learn about the * command
The problem states we don't have to exceed 4 arguments, I use the cd /c* to cd into the challenge after that I ran the ./r* whcih matches with run

    Connected!                                                                        
    This challenge resets your working directory to /home/hacker unless you change 
    directory properly...
    hacker@globbing~matching-with-:~$ cd /c*
    hacker@globbing~matching-with-:/challenge$ ./r*
    You ran me with the working directory of /challenge! Here is your flag:
    pwn.college{oGiRRfMEGBOG8-Uh2xv6LC6eNVQ.dFjM4QDL4ETO0czW}

## Matching with ?

In this problem we get to learn about the ? command 
The problem suggest us to first cd into /challeng by using the /??ha??enge, as the characters to be ommited are hidden by wildcard
I use ./run to get the flag 

    hacker@globbing~matching-with-:~$ cd /challenge
    You used either the 'c', 'l', or '*' characters. Disallowed!
    This challenge resets your working directory to /home/hacker unless you change 
    directory properly...
    hacker@globbing~matching-with-:~$ cd /?ha??enge
    hacker@globbing~matching-with-:/challenge$ ./run
    You ran me with the working directory of /challenge! Here is your flag:
    pwn.college{4MR9umUXBDY5nQERqzMgDBnMspw.dJjM4QDL4ETO0czW}
    hacker@globbing~matching-with-:/challenge$ 

## Matching with []

The [] matches with the unique characters
I ran the command cd to /challenge/files as given 
I ran /challenge/run file_[bash] as it will match file_b file_a file_s file_h

    Connected!                                                                        
    hacker@globbing~matching-with-:~$ cd /challenge/files
    hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
    You got it! Here is your flag!
    pwn.college{o1YicVgxPNP9SD23FGX1ednlb9K.dNjM4QDL4ETO0czW}

## Matching Paths With []

As from the pervious program the change in this name tell us that this builds on the last one, but we have to match the path not the files
to being this we start with   /challenge/run with the path to all the files
Now we have to provide the syntax with the absolute path 

    Connected!                                                                        
    hacker@globbing~matching-paths-with-:~$ /challenge/run 
    Error: you did not use a square bracket glob...
    hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
    You got it! Here is your flag!
    pwn.college{caX_b5aYNpnN8yHrLILAppBo1Qt.dRjM4QDL4ETO0czW}

## Mixing Globs

This is a tough one as it sums up to all forms of globbing to get the flag 
I switch the working directory to /challenge/files
as [] goes through all the cycles as a single character, and then adding up * to this would work as wildcard 

    Connected!                                                                        
    hacker@globbing~mixing-globs:~$ /challenge/files
    ssh-entrypoint: /challenge/files: Is a directory
    hacker@globbing~mixing-globs:~$ cd /challenge/files
    hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
    You got it! Here is your flag!
    pwn.college{oPgkzfBCBxQJ6Bw9ErwCYWhZb3T.dVjM4QDL4ETO0czW}

## Exclusionary Globbing

In this it tells us to exclude some files in the glob by using ^ or !
I start with cd into /challenge/files to cd /challenge/files
Then we need to do the same thing just added a ^ to pwn --> /challenge/run [^pwn]

    Connected!                                                                        
    /chacker@globbing~exclusionary-globbing:~$ /challenge/files
    ssh-entrypoint: /challenge/files: Is a directory
    hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
    hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [^pwn]*
    You got it! Here is your flag!
    pwn.college{4W-UahAXG0eD65WAnIRdYwbfuEi.dZjM4QDL4ETO0czW}
