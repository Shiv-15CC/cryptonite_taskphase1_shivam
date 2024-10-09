# PRACTICING PIPING

## Redirecting Output

The piping feature allows user to redirect input,output and errors which could be used in other programs
To start off with I first ran the echo PWN which gave me PWN after which i executed echo PWN>COLLEGE from which i got the flag 

    Connected!                                                                        
    hacker@piping~redirecting-output:~$ echo PWN
    PWN
    hacker@piping~redirecting-output:~$ echo PWN>COLLEGE
    Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your 
    flag:
    pwn.college{w6xT8h-6o3y2IhxGecXK8q9fhpD.dRjN1QDL4ETO0czW}

## Redirecting More Output

This probelm is just an advance of the previous one
In this I just redirected to /challenge/run output to my myflag by, /challenge/run > myflag
Then to read into the myflag we need to run cay myflag command which gives the flag.

    Connected!                                                                        
    hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
    [INFO] WELCOME! This challenge makes the following asks of you:
    [INFO] - the challenge will check that output is redirected to a specific file path : myflag
    [INFO] - the challenge will output a reward file if all the tests pass : /flag

    [HYPE] ONWARDS TO GREATNESS!
  
    [INFO] This challenge will perform a bunch of checks.
    [INFO] If you pass these checks, you will receive the /flag file.

    [TEST] You should have redirected my stdout to a file called myflag. Checking...

    [PASS] The file at the other end of my stdout looks okay!
    [PASS] Success! You have satisfied all execution requirements.
    hacker@piping~redirecting-more-output:~$ cat myflag

    [FLAG] Here is your flag:
    [FLAG] pwn.college{QcS9UYobDGOO3KRZ6wo9gS2EjKY.dVjN1QDL4ETO0czW}


## Appending Output

As > turns over with output, >> will append the result to the remaning of the file
Instead of using > I used >> and ran /challenge/run >> ~/the-flag-
And then printed the flag by cat ~/file

    hacker@piping~appending-output:~$ /challenge/run >> ~/the-flag
    [INFO] WELCOME! This challenge makes the following asks of you:
    [INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

    [HYPE] ONWARDS TO GREATNESS!

    [INFO] This challenge will perform a bunch of checks.
    [INFO] Good luck!

    [TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...
    
    [HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
    [HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
    [HINT] creating and trying to pass in FDs in python.

    [PASS] The file at the other end of my stdout looks okay!
    [PASS] Success! You have satisfied all execution requirements.
    I will write the flag in two parts to the file /home/hacker/the-flag! I'll do 
    the first write directly to the file, and the second write, I'll do to stdout 
    (if it's pointing at the file). If you redirect the output in append mode, the 
    second write will append to (rather than overwrite) the first write, and you'll 
    get the whole flag!
    hacker@piping~appending-output:~$ cat ~/the-flag
     | 
    \|/ This is the first half:
     v 
    pwn.college{4g5s2mhz2JARg-OMy90V55f8m4M.ddDM5QDL4ETO0czW}
                                 ^
        that is the second half /|\
                                 |

    If you only see the second half above, you redirected in *truncate* mode (>) 
    rather than *append* mode (>>), and so the write of the second half to stdout 
    overwrote the initial write of the first half directly to the file. Try append 
    mode!


## Redirecting Errors

In this we will learn about the The File DesCriptor Number 
As told in the problem we need to use the 2> operator 
To start with I ran /challenge/run > myflag 2> instructions
To print the flag use cat my flag 

    Connected!                                                                        
    hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
    hacker@piping~redirecting-errors:~$ /challenge/run > myflag
    [INFO] WELCOME! This challenge makes the following asks of you:
    [INFO] - the challenge will check that output is redirected to a specific file path : myflag
    [INFO] - the challenge will check that error output is redirected to a specific file path : instructions
    [INFO] - the challenge will output a reward file if all the tests pass : /flag

    [HYPE] ONWARDS TO GREATNESS!

    [INFO] This challenge will perform a bunch of checks.
    [INFO] If you pass these checks, you will receive the /flag file.

    [TEST] You should have redirected my stdout to a file called myflag. Checking...

    [PASS] The file at the other end of my stdout looks okay!

    [TEST] You should have redirected my stderr to instructions. Checking...

    [FAIL] You did not satisfy all the execution requirements.
    [FAIL] Specifically, you must fix the following issue:
    [FAIL]   You have not redirected anything for this process' stderr.
    hacker@piping~redirecting-errors:~$ cat my flag 
    cat: my: No such file or directory
    cat: flag: No such file or directory
    hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
    hacker@piping~redirecting-errors:~$ cat myflag

    [FLAG] Here is your flag:
    [FLAG] pwn.college{EsvBxZcllBUSFwsM4a-qZ8wFGdE.ddjN1QDL4ETO0czW}


## Redirecting Input 

As we can redirect the outputs we can also redirect the input
I first ran PWN which conatins COLLEGE-> echo COLLEGE > PWN
I then redirect PWN to /challeng/run as input /challenge/run < PWN

    Connected!                                                                        
    hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
    hacker@piping~redirecting-input:~$ /challenge/run < PWN
    Reading from standard input...
    Correct! You have redirected the PWN file into my standard input, and I read 
    the value 'COLLEGE' out of it!
    Here is your flag:
    pwn.college{QzxmqrxD2c1ZoInCPrhnOBBNxwY.dBzN1QDL4ETO0czW}
    

## Grepping Stored Rwults

We have till now learned about how to run commands, how to redirect output and search in the resulting file 
First I have /challeng/run output redirected to /tmp/data.txt
I then grep for pwn.college as its there in all keys -> grep pwn.college /tmp/data/txt


    Connected!                                                                        
    hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
    [INFO] WELCOME! This challenge makes the following asks of you:
    [INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
    [INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

    [HYPE] ONWARDS TO GREATNESS!

    [INFO] This challenge will perform a bunch of checks.
    [INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

    [TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

    [HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
    [HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
    [HINT] creating and trying to pass in FDs in python.

    [PASS] The file at the other end of my stdout looks okay!
    [PASS] Success! You have satisfied all execution requirements.
    hacker@piping~grepping-stored-results:~$ grep pwn.college /tmp/data.txt
    pwn.college{EYKU-pYMtbZB59Vc-3Wbrlg2ImO.dhTM4QDL4ETO0czW}
    hacker@piping~grepping-stored-results:~$ 


## Grepping Live Output 

As per the last problem we had to redirect the output to /tmp/data.txt but in this it wants us to pipe, bascially redirect the output of /challege/run to the grep argument through pipes
To start with /challenge/run | greps to the output to grep pwn.college as an argument 

    Connected!                                                                        
    hacker@piping~grepping-live-output:~$ /challenge/run | grep pwn.college
    [INFO] WELCOME! This challenge makes the following asks of you:
    [INFO] - the challenge checks for a specific process at the other end of stdout : grep
    [INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

    [HYPE] ONWARDS TO GREATNESS!

    [INFO] This challenge will perform a bunch of checks.
    [INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

    [TEST] You should have redirected my stdout to another process. Checking...
    [TEST] Performing checks on that process!

    [INFO] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep.
    [INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
    [INFO] To pass the checks, the executable must be grep.

    [PASS] You have passed the checks on the process on the other end of my stdout!
    [PASS] Success! You have satisfied all execution requirements.
    pwn.college{cl6m5YdZ6NoNt9_xVezaL5yovUj.dlTM4QDL4ETO0czW}


## Grepping Errors

This probelem tells us ways of converting a file decriptor to another file descriptor as there is no 2| operator
we have to do it on our own by running 2>&1

    Connected!                                                                        
    hacker@piping~grepping-errors:~$ /challenge/run 2>&1 | grep pwn.college
    [INFO] WELCOME! This challenge makes the following asks of you:
    [INFO] - the challenge checks for a specific process at the other end of stderr : grep
    [INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt
    
    [HYPE] ONWARDS TO GREATNESS!
    
    [INFO] This challenge will perform a bunch of checks.
    [INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

    [TEST] You should have redirected my stderr to another process. Checking...
    [TEST] Performing checks on that process!

    [INFO] The process' executable is /nix/store/xpq4yhadyhazkcsggmqd7rsgvxb3kjy4-gnugrep-3.11/bin/grep.
    [INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
    [INFO] To pass the checks, the executable must be grep.

    [PASS] You have passed the checks on the process on the other end of my stderr!
    [PASS] Success! You have satisfied all execution requirements.
    pwn.college{E2q7JAMlQ8IcOscfFh4rtXob1oX.dVDM5QDL4ETO0czW}


## Duplicating Piped Data with tee

This problem introduces us to the tee command in which it allows us to  disable how the output moves through the pipes 
After reading and all i started to work by using a dummy file output 
reading the output file by cat output 
/challenge/pwn needs a secret argument 
then I execute /challege/pwn --secret  | /challenge/college to get the flag 

    Connected!                                                                        
    hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn |tee output | /challenge/college
    Processing...
    The input to 'college' does not contain the correct secret code! This code 
    should be provided by the 'pwn' command. HINT: use 'tee' to intercept the 
    output of 'pwn' and figure out what the code needs to be.
    hacker@piping~duplicating-piped-data-with-tee:~$ cat output 
    Usage: /challenge/pwn --secret [SECRET_ARG]

    SECRET_ARG should be "IGp3MDK8"
    hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret IGp3MDK8
    Processing...
    You must pipe the output of /challenge/pwn into /challenge/college (or 'tee' 
    for debugging).
    hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret IGp3MDK8 | /challeneg/college
    ssh-entrypoint: /challeneg/college: No such file or directory
    Processing...
    You must pipe the output of /challenge/pwn into /challenge/college (or 'tee' 
    for debugging).
    hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret IGp3MDK8 | /challenge/college
    Processing...
    Correct! Passing secret value to /challenge/college...
    Great job! Here is your flag:
    pwn.college{IGp3MDK83LAfqxeRojL7Mfr9-SA.dFjM5QDL4ETO0czW}


## Writing To Multiple Programs

This problem allows us to directly send stuff from error or output to input to the of the program,
First we start with /challenge/the, the input path 
the pipe is t is splitted into /challenge/planet as an argument
now /challenge/hack for output through pipes
the main command would be challeneg/hacl | tee>(/challenge/the) | /challenge/planet 

    Connected!                                                                        
    hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) | /challenge/planet 
    Congratulations, you have duplicated data into the input of two programs! Here 
    is your flag:
    pwn.college{g_pRbitjMbeJbbTK7VuMpgo7fp9.dBDO0UDL4ETO0czW}


## Split-Pipping stderr and stdout

This is a mind problem cause for this understanding of the file descriptor operators is necsessary,
As the stderr of the /challennge/hack has to go to /challenge/the as in the input, I use 2> to send stderr and >(/challenge/the) 
for the stdout of /challenge/hack has to go to /challenge/planet as inpput, i use > to send stdout and >(/challenge/planet)   

    Connected!                                                                        
    hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack 2> >(/challenge/the) > >(/challenge/planet)
    Congratulations, you have learned a redirection technique that even experts 
    struggle with! Here is your flag:
    pwn.college{YVPd6nDe8uKsb042E4uttP5wriJ.dFDNwYDL4ETO0czW}
