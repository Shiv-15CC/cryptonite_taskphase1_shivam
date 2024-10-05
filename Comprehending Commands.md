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


