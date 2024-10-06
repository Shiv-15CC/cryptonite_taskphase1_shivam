# Comprehending Commands

## cat:not the pet, but the command!

For this one we bascially use the cat flag command to view the contents of a file 

    Connected!                                                                        
    hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag 
    pwn.college{MZ52dKywLeTJSLNwUPZH7ZAabqQ.dFzN1QDL4ETO0czW}

## catting absolute paths

This is same as the above one but the difference is that in this we need to use the absolute path of /flag as an argument 

    Connected!                                                                        
    hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag 
    pwn.college{MZ52dKywLeTJSLNwUPZH7ZAabqQ.dFzN1QDL4ETO0czW}

## more catting practice

In this catting practice we can't use the cd command so for this i used the cd command to get a new directory but to change the directory I was required to use the cat /usr/share/initramfs-tools/flag, which was given by the system itself 

    Connected!                                                                        
    You cannot use the 'cd' command in this level, and must retrieve the flag by 
    absolute path. Plus, I hid the flag in a different directory! You can find it 
    in the file /usr/share/initramfs-tools/flag. Go cat it out **without** cding 
    into that directory!
    hacker@commands~more-catting-practice:~$ cd 
    You used 'cd'! In this level, I don't allow you to change the working directory 
    --- you MUST chase pass 'cat' the absolute path of where I put it on the 
    filesystem (which is /usr/share/initramfs-tools/flag).
    hacker@commands~more-catting-practice:~$ cd /usr/share/initramfs-tools/flag
    You used 'cd'! In this level, I don't allow you to change the working directory 
    --- you MUST chase pass 'cat' the absolute path of where I put it on the 
    filesystem (which is /usr/share/initramfs-tools/flag).
    hacker@commands~more-catting-practice:~$ cat /usr/share/initramfs-tools/flag
    pwn.college{QiJtsRMu_SOCsDelPbQchiNFAHf.dBjM5QDL4ETO0czW}

## grepping for needle in a hacksystem 

This is a new command grep which allws us to search for the content 

    Connected!                                                                        
    hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
    pwn.college{IeH8ejrayVIocp6Xfd2Fa5jzj22.ddTM4QDL4ETO0czW}

## listing files 

In this we were introduced to the ls command, whcih lists out all the content in that cureent directory in whcih we are working 
to start for this as directed i first used the ls /challenge command to find the content present in the challenge directory after which i used the run command on using that i got to know it was changed to 2724-renamed-run-18691, after which i used the /challenge/2724-renamed-run-18691 for getting a flag 

    Connected!                                                                        
    hacker@commands~listing-files:~$ ls /challenge
    2724-renamed-run-18691  DESCRIPTION.md
    hacker@commands~listing-files:~$ /challenge/2724-renamed-run-18691
    Yahaha, you found me! Here is your flag:
    pwn.college{8WmL5eeX4gSA5FS5GjuwT0j8Ous.dhjM4QDL4ETO0czW}

## touching files

In this we will be creating a new file by the touch command
To start off with i frst used the cd /temp to change the directory after which as stated we need to create two new files - touch pwn and touch college, after making the two files just run the /challenge/run command to get the flag

    Connected!                                                                        
    hacker@commands~touching-files:~$ cd /tmp
    hacker@commands~touching-files:/tmp$ touch pwn
    hacker@commands~touching-files:/tmp$ touch college
    hacker@commands~touching-files:/tmp$ /challenge/run
    Success! Here is your flag:
    pwn.college{Q6tkUsczpLreKxXLq-WDEliQWHb.dBzM4QDL4ETO0czW}

## removing files

As we get to know by the name removing files, when there are a excess of files around us we need to clear them so for that there is the command rm 
To start with this I first used the rm delete_me as told, following with the /challenge/run command 

    Connected!                                                                        
    hacker@commands~removing-files:~$ rm delete_me
    hacker@commands~removing-files:~$ /challenge/check 
    Excellent removal. Here is your reward:
    pwn.college{sB-xcLKo59I9es0xLmzr7VBxCVS.dZTOwUDL4ETO0czW}

## hidden files

In this we got to know a new thing that ls doesn't list all the files some of them are hidden, so to find those hidden files we need to invoke it with a -a flag 
these are those files which start with a .(dot)

In this i change the directory from / to cd /
then I list all the files ls -a

    Connected!                                                                        
    hacker@commands~hidden-files:~$ cd /
    hacker@commands~hidden-files:/$ ls -a
    .  ..  .dockerenv  .flag-149532542219529  bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
    hacker@commands~hidden-files:/$ cat .flag-149532542219529
    pwn.college{kwDsaUYrBOdNf5sHwRavbkshCkf.dBTN4QDL4ETO0czW}

## An Epic Filesystem Quest 

## Making directories 

In this we learnt a new command which is the making directories by mkdir 
As told I first made a directory with /tmp/pwn after which i change the current directory to it by cd /tmp/pwn after which i ran the touch college command and for the final command i used the /challenge/run to get the flag 

    Connected!                                                                        
    hacker@commands~making-directories:~$ mkdir /tmp/pwn
    hacker@commands~making-directories:~$ cd /tmp/pwn
    hacker@commands~making-directories:/tmp/pwn$ touch college
    hacker@commands~making-directories:/tmp/pwn$ /challenge/run
    Success! Here is your flag:
    pwn.college{YU52bEF_seE7-oEs78XEQ_iajAC.dFzM4QDL4ETO0czW}

## finding files

In this we use the find command to find the files or directories 
to run this first we need to run the find / -name flag command which helps us to find the files or directories which start with the word flag 
after which we need to cat command 

    Connected!                                                                        
    hacker@commands~finding-files:~$ find / -name flag
    find: ‘/root’: Permission denied
    find: ‘/proc/1/task/1/fd’: Permission denied
    find: ‘/proc/1/task/1/fdinfo’: Permission denied
    find: ‘/proc/1/task/1/ns’: Permission denied
    find: ‘/proc/1/fd’: Permission denied
    find: ‘/proc/1/map_files’: Permission denied
    find: ‘/proc/1/fdinfo’: Permission denied
    find: ‘/proc/1/ns’: Permission denied
    find: ‘/proc/7/task/7/fd’: Permission denied
    find: ‘/proc/7/task/7/fdinfo’: Permission denied
    find: ‘/proc/7/task/7/ns’: Permission denied
    find: ‘/proc/7/fd’: Permission denied
    find: ‘/proc/7/map_files’: Permission denied
    find: ‘/proc/7/fdinfo’: Permission denied
    find: ‘/proc/7/ns’: Permission denied
    find: ‘/var/log/private’: Permission denied
    find: ‘/var/log/apache2’: Permission denied
    find: ‘/var/log/mysql’: Permission denied
    find: ‘/var/cache/ldconfig’: Permission denied
    find: ‘/var/cache/apt/archives/partial’: Permission denied
    find: ‘/var/cache/private’: Permission denied
    find: ‘/var/lib/apt/lists/partial’: Permission denied
    find: ‘/var/lib/php/sessions’: Permission denied
    find: ‘/var/lib/mysql-files’: Permission denied
    find: ‘/var/lib/private’: Permission denied
    find: ‘/var/lib/mysql-keyring’: Permission denied
    find: ‘/var/lib/mysql’: Permission denied
    find: ‘/tmp/tmp.XvrUsDZh8M’: Permission denied
    find: ‘/run/mysqld’: Permission denied
    find: ‘/run/sudo’: Permission denied
    find: ‘/etc/ssl/private’: Permission denied
    /usr/local/lib/python3.8/dist-packages/sympy/combinatorics/flag
    /usr/local/lib/python3.8/dist-packages/pwnlib/flag
    /usr/local/share/radare2/5.9.5/flag
    /opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
    /opt/radare2/libr/flag
    /nix/store/pmvk2bk4p550w182rjfm529kfqddnvh3-python3.11-pwntools-4.12.0/lib/python3.11/site-packages/pwnlib/flag
    /nix/store/1yagn5s8sf7kcs2hkccgf8d0wxlrv5sz-radare2-5.9.0/share/radare2/5.9.0/flag
    hacker@commands~finding-files:~$ cat /usr/local/share/radare2/5.9.5/flag
    cat: /usr/local/share/radare2/5.9.5/flag: Is a directory
    hacker@commands~finding-files:~$ cat /usr/local/lib/python3.8/dist-packages/pwnlib/flag
    cat: /usr/local/lib/python3.8/dist-packages/pwnlib/flag: Is a directory
    hacker@commands~finding-files:~$ cat /usr/local/lib/python3.8/dist-packages/sympy/combinatorics/flag
    pwn.college{4Zgvpea_YeRmrKVhj7yfS-VQZdh.dJzM4QDL4ETO0czW}
    hacker@commands~finding-files:~$ 

## linking files 

In this program we start off with ln -s /flag /home/hacker/not-the/flag, after this i executed the /challenge/catflag to get the key

    Connected!                                                                        
    hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
    hacker@commands~linking-files:~$ /challenge/catflag
    About to read out the /home/hacker/not-the-flag file!
    pwn.college{Qdg5ZsVYDKzvPZ4dtknbcipdwdH.dlTM1UDL4ETO0czW}



