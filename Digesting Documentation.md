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
 
## Searching Manuals

This is same as the previous program just the difference is that in this there is a hidden argument 
We start with 'man challenge'
after a lot of understanding I found the cieo argument 
I executed the /challenge/challenge --cieo to get the flag

    shivam-mit@shivam-mit-Inspiron-7373:~$ ssh -i ./key hacker@dojo.pwn.college
    Connected!                                                                        
    hacker@man~searching-manuals:~$ man chllenge
    No manual entry for chllenge
    hacker@man~searching-manuals:~$ man challenge
    hacker@man~searching-manuals:~$ /challenge/challenge --cieo
    Initializing...
    Correct usage! Your flag: pwn.college{s2wQrdZN1GjiM7aqKTpEULidIRd.dVTM4QDL4ETO0czW}

## Searching for Manuals

This problem is slightly tricky to get to the flag, but yes eventually u will land there soon 
To start off with first we run is man man I directed
After finding for a long time i came across the man -K 
after whcih i ran the man -K/challenge/challenge to search for manauals that reference the string. 
Finally after finding the document I found the --avhzee argument 
After whcih i ran the /challenge/challenge --avhzee 052 to get the flag 

    shivam-mit@shivam-mit-Inspiron-7373:~$ ssh -i ./key hacker@dojo.pwn.college
    Connected!                                                                        
    hacker@man~searching-for-manuals:~$ man -K "challenge/challenge"

    CHALLENGE(1)                                                                     Challenge Commands                                                                               CHALLENGE(1)

    NAME
       /challenge/challenge - print the flag!

    SYNOPSIS
       challenge OPTION

    DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --avhzee NUM
              print the flag if NUM is 052

    AUTHOR
       Written by Zardus.

    REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-luminarium/>

    SEE ALSO
       man(1) bash-builtins(7)

     pwn.college                                                                           May 2024                                                                                        CHALLENGE(1)
    chacker@man~searching-for-manuals:~$ ^C
    hacker@man~searching-for-manuals:~$ /challenge/challenge  --avhzee 052
    Correct usage! Your flag: pwn.college{0XavZHXGhX5zePFKe2d1XjNGPRU.dZTM4QDL4ETO0czW}


## Helpful Programs 

Many command don't have the 'man' command so in that case we use the help command which is the --help 
For this we start with '/challenge/challenge --help
after that we use the '/challenge/challenge -p' which give the value of '-g'
after getting the value of g which in my case is 309 
I ran the '/challenge/challenge -g 309' command to get the flag 

    Connected!                                                                        
    hacker@man~helpful-programs:~$ /challenge/challenge --help
    usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

    optional arguments:
    -h, --help            show this help message and exit
    --fortune             read your fortune
    -v, --version         get the version number
    -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
    -p, --print-value     print the value that will cause the -g option to give you the flag
    hacker@man~helpful-programs:~$ /challenge/challenge -p
    The secret value is: 309
    hacker@man~helpful-programs:~$ /challenge/challenge -g 309
    Correct usage! Your flag: pwn.college{cjg-3Z0P99ixRmOh1vLV-HYqdmt.ddjM4QDL4ETO0czW}

## Help For Builtins 

In this problem we learnt the builtins, which are built into the shell itself 
To start off with we run the help command after which i found challenge 
I ran the help challenge command to get more details about the challenge 
Then finally I got the secret and then ran hallenge --secret"U_tTUZek"


    Connected!                                                                        
    hacker@man~help-for-builtins:~$ help
    GNU bash, version 5.2.32(1)-release (x86_64-pc-linux-gnu)
    These shell commands are defined internally.  Type `help' to see this list.
    Type `help name' to find out more about the function `name'.
    Use `info bash' to find out more about the shell in general.
    Use `man -k' or `info' to find out more about commands not in this list.

    A star (*) next to a name means that the command is disabled.

    job_spec [&]                                                                                history [-c] [-d offset] [n] or history -anrw [filename] or history -ps arg           [arg...]
    (( expression ))                                                                            if COMMANDS; then COMMANDS; [ elif COMMANDS; then COMMANDS; ]... [ else COMMANDS;     ] fi
    . filename [arguments]                                                                      jobs [-lnprs] [jobspec ...] or jobs -x command [args]
    :                                                                                           kill [-s sigspec | -n signum | -sigspec] pid | jobspec ... or kill -l [sigspec]
    [ arg... ]                                                                                  let arg [arg ...]
    [[ expression ]]                                                                            local [option] name[=value] ...
    alias [-p] [name[=value] ... ]                                                              logout [n]
     bg [job_spec ...]                                                                           mapfile [-d delim] [-n count] [-O origin] [-s count] [-t] [-u fd] [-C callback]      [-c quan>
     bind [-lpsvPSVX] [-m keymap] [-f filename] [-q name] [-u name] [-r keyseq] [-x keyseq:she>  popd [-n] [+N | -N]
     break [n]                                                                                   printf [-v var] format [arguments]
     builtin [shell-builtin [arg ...]]                                                           pushd [-n] [+N | -N | dir]
     caller [expr]                                                                               pwd [-LP]
     case WORD in [PATTERN [| PATTERN]...) COMMANDS ;;]... esac                                  read [-ers] [-a array] [-d delim] [-i text] [-n nchars] [-N nchars] [-p prompt]      [-t time>
    cd [-L|[-P [-e]] [-@]] [dir]                                                                readarray [-d delim] [-n count] [-O origin] [-s count] [-t] [-u fd] [-C callback]     [-    c qu>
     challenge [--fortune] [--version] [--secret SECRET]                                         readonly [-aAf] [name[=value] ...] or readonly -p
     command [-pVv] command [arg ...]                                                            return [n]
     compgen [-abcdefgjksuv] [-o option] [-A action] [-G globpat] [-W wordlist] [-F function] >  select NAME [in WORDS ... ;] do COMMANDS; done
     complete [-abcdefgjksuv] [-pr] [-DEI] [-o option] [-A action] [-G globpat] [-W wordlist] >  set [-abefhkmnptuvxBCEHPT] [-o option-name] [--] [-] [arg ...]
     compopt [-o|+o option] [-DEI] [name ...]                                                    shift [n]
     continue [n]                                                                                shopt [-pqsu] [-o] [optname ...]
     coproc [NAME] command [redirections]                                                        source filename [arguments]
     declare [-aAfFgiIlnrtux] [name[=value] ...] or declare -p [-aAfFilnrtux] [name ...]         suspend [-f]
     dirs [-clpv] [+N] [-N]                                                                      test [expr]
     disown [-h] [-ar] [jobspec ... | pid ...]                                                   time [-p] pipeline
     echo [-neE] [arg ...]                                                                       times
     enable [-a] [-dnps] [-f filename] [name ...]                                                trap [-lp] [[arg] signal_spec ...]
     eval [arg ...]                                                                              true
     exec [-cl] [-a name] [command [argument ...]] [redirection ...]                             type [-afptP] name [name ...]
     exit [n]                                                                                    typeset [-aAfFgiIlnrtux] name[=value] ... or typeset -p [-aAfFilnrtux] [name ...]
     export [-fn] [name[=value] ...] or export -p                                                ulimit [-SHabcdefiklmnpqrstuvxPRT] [limit]
     false                                                                                       umask [-p] [-S] [mode]
     fc [-e ename] [-lnr] [first] [last] or fc -s [pat=rep] [command]                            unalias [-a] name [name ...]
     fg [job_spec]                                                                               unset [-f] [-v] [-n] [name ...]
     for NAME [in WORDS ... ] ; do COMMANDS; done                                                until COMMANDS; do COMMANDS-2; done
     for (( exp1; exp2; exp3 )); do COMMANDS; done                                               variables - Names and meanings of some shell variables
     function name { COMMANDS ; } or name () { COMMANDS ; }                                      wait [-fn] [-p var] [id ...]
     getopts optstring name [arg ...]                                                            while COMMANDS; do COMMANDS-2; done
     hash [-lr] [-p pathname] [-dt] [name ...]                                                   { COMMANDS ; }
     help [-dms] [pattern ...]
    hacker@man~help-for-builtins:~$ help challenge
    challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!
    
    Options:
      --fortune		display a fortune
      --version		display the version
      --secret VALUE	prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "U_tTUZek".
    hacker@man~help-for-builtins:~$ challenge --secret U_tTUZek
    Correct! Here is your flag!
    pwn.college{U_tTUZekrwkmYX-nzBrkGG01HEg.dRTM5QDL4ETO0czW}
