# SHELL VARIABLES

## Printing Variables:
This module helps us in learning a new language which helps us to interact with linux commands
#### Method
As the Problem told use FLAG with echo $FLAG to get the flag
```bash
Connected!                                                                        
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{ohBTjh7BjebDkptKl2MpIq-U-V2.ddTN1QDL4ETO0czW}
```

## Setting Variables
As the last problem is printing variables in this we will set a value of them.
#### Method
Assign COLLEGE as value to PWN, and as told further PWN=COLLEGE
```bash
Connected!
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{Y37SKw1RwODbcqtADG-Pkw0c1TS.dlTN1QDL4ETO0czW}
```
## Multi-word Variables
This is a extension of the previous one in which the varibles will be assigned multi-word values.
#### Method
Set COLLEGE YEAH to PWN, now these are 2 words so we use "COLLEGE YEAH" when setting it , PWN="COLLEGE YEAH"
```bash
Connected!
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{YUjPia3HKIipGJNbowJWEnrc0NZ.dBjN1QDL4ETO0czW}
hacker@variables~multi-word-variables:~$ 
```

## Exporting Variables
Helps us to export variables from another shell when in use.
#### Method
- PWN=COLLEGE
- Then assign COLLEGE=PWN
- The problem told to export the PWN variables, export PWM
- get the flag finally, /challenge/run
```bash
Connected!
hacker@variables~exporting-variables:~$ PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ export PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{0ocX52fkTrChUWO4ao17lU4K1qb.dJjN1QDL4ETO0czW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ 
```

## Printing Exported Variables
In This the command env helps us to print out all the exported variables set in the shell
#### Method
TO start with use env command to print all he exported variables, the flag is given in the list
```bash
                                                                                                                                                                Connected!
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
DOJO_AUTH_TOKEN=ecaae0d6c9802a5e23b225588124da11e9d138e1367d5c7767a4d38ae8cfc51e
HOME=/home/hacker
LANG=C.UTF-8
LS_COLORS=rs=0:di=01;34:ln=01;36:mh=00:pi=40;33:so=01;35:do=01;35:bd=40;33;01:cd=40;33;01:or=40;31;01:mi=00:su=37;41:sg=30;43:ca=00:tw=30;42:ow=34;42:st=37;44:ex=01;32:*.7z=01;31:*.ace=01;31:*.alz=01;31:*.apk=01;31:*.arc=01;31:*.arj=01;31:*.bz=01;31:*.bz2=01;31:*.cab=01;31:*.cpio=01;31:*.crate=01;31:*.deb=01;31:*.drpm=01;31:*.dwm=01;31:*.dz=01;31:*.ear=01;31:*.egg=01;31:*.esd=01;31:*.gz=01;31:*.jar=01;31:*.lha=01;31:*.lrz=01;31:*.lz=01;31:*.lz4=01;31:*.lzh=01;31:*.lzma=01;31:*.lzo=01;31:*.pyz=01;31:*.rar=01;31:*.rpm=01;31:*.rz=01;31:*.sar=01;31:*.swm=01;31:*.t7z=01;31:*.tar=01;31:*.taz=01;31:*.tbz=01;31:*.tbz2=01;31:*.tgz=01;31:*.tlz=01;31:*.txz=01;31:*.tz=01;31:*.tzo=01;31:*.tzst=01;31:*.udeb=01;31:*.war=01;31:*.whl=01;31:*.wim=01;31:*.xz=01;31:*.z=01;31:*.zip=01;31:*.zoo=01;31:*.zst=01;31:*.avif=01;35:*.jpg=01;35:*.jpeg=01;35:*.mjpg=01;35:*.mjpeg=01;35:*.gif=01;35:*.bmp=01;35:*.pbm=01;35:*.pgm=01;35:*.ppm=01;35:*.tga=01;35:*.xbm=01;35:*.xpm=01;35:*.tif=01;35:*.tiff=01;35:*.png=01;35:*.svg=01;35:*.svgz=01;35:*.mng=01;35:*.pcx=01;35:*.mov=01;35:*.mpg=01;35:*.mpeg=01;35:*.m2v=01;35:*.mkv=01;35:*.webm=01;35:*.webp=01;35:*.ogm=01;35:*.mp4=01;35:*.m4v=01;35:*.mp4v=01;35:*.vob=01;35:*.qt=01;35:*.nuv=01;35:*.wmv=01;35:*.asf=01;35:*.rm=01;35:*.rmvb=01;35:*.flc=01;35:*.avi=01;35:*.fli=01;35:*.flv=01;35:*.gl=01;35:*.dl=01;35:*.xcf=01;35:*.xwd=01;35:*.yuv=01;35:*.cgm=01;35:*.emf=01;35:*.ogv=01;35:*.ogx=01;35:*.aac=00;36:*.au=00;36:*.flac=00;36:*.m4a=00;36:*.mid=00;36:*.midi=00;36:*.mka=00;36:*.mp3=00;36:*.mpc=00;36:*.ogg=00;36:*.ra=00;36:*.wav=00;36:*.oga=00;36:*.opus=00;36:*.spx=00;36:*.xspf=00;36:*~=00;90:*#=00;90:*.bak=00;90:*.crdownload=00;90:*.dpkg-dist=00;90:*.dpkg-new=00;90:*.dpkg-old=00;90:*.dpkg-tmp=00;90:*.old=00;90:*.orig=00;90:*.part=00;90:*.rej=00;90:*.rpmnew=00;90:*.rpmorig=00;90:*.rpmsave=00;90:*.swp=00;90:*.tmp=00;90:*.ucf-dist=00;90:*.ucf-new=00;90:*.ucf-old=00;90:
FLAG=pwn.college{QSRmjRtQvawvTp3YVZXAPqaFc9I.dhTN1QDL4ETO0czW}
LESSCLOSE=/usr/bin/lesspipe %s %s
TERM=xterm
LESSOPEN=| /usr/bin/lesspipe %s
SHLVL=1
LC_CTYPE=C.UTF-8
PATH=/run/challenge/bin:/run/workspace/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
_=/run/workspace/bin/env
hacker@variables~printing-exported-variables:~$ 
```

## Storing Command Output
This allows us to directly store a program's output in a variables
#### Method
to start with use /challenge/run output in PWN, executing PWN=$(/challenge/run), After that print PWN using echo $PWN
```bash
Connected!                                                                        
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{MZJMu6zkGflaFB7akwc0whnm91q.dVzN0UDL4ETO0czW}
hacker@variables~storing-command-output:~$ 
```

## Reading Input
This allows us to user to give the input
#### Method
Start with read -p "Enter Values:"PWN to read the input into PWN variables, then enter COLLEGE as the flag
```bash
Connected!
hacker@variables~reading-input:~$ read -p "Enter Value:" PWN
Enter Value:COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{Y-lnrYOWMMOE_-iqsSdNMfaiZKe.dhzN1QDL4ETO0czW}
hacker@variables~reading-input:~$ 
```
## Reading Files
This commands allows us to directly redirect a file into a variables std input
#### Method
As the probelm suggested execute read PWN< /challenge/read_me to redirect /challenge/read_me as the input to PWN
```bash
Connected!
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{8u89C6lLl9UY1lXy4a0MEKK8Miy.dBjM4QDL4ETO0czW}
hacker@variables~reading-files:~$ 
```
