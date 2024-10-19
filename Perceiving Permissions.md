# Perceiving Permissions

## Changing File Ownership
In this module it helps us to explain about handling permissions of files
#### Method
- We need to change the owner of /flag to hacker by using chown hacker /flag
- We get the flag by cat /flag
```bash

```

## Groups and Files
In this problem we see the involvement of changing the group ownership of a file using chgrp
#### Method
- Check the group id using id, there are 1000
- Change the ownership to group 1000 using chgrp 1000/flag
- Get the flag by cat /flag
```bash

```
## Fun With Groups Names
This is same as the previous one in this we just need to figure our the group we are in and it's id before changing ownership
#### Method
- Use id to get some information 
- The group name grp21385 seems like that is the grp, hence 1000 will be the group id
- Execute chgrp 1000 /flag to change ownership of the flag to group with id 1000
- Get the flag using cat /flag
```bash

```

## Changing Permissions
In this problem we need to change the permission of the/flag file
#### Method
- I start by giving all users read permission using o+r /flag 
- I get the flag by cat /flag

```bash

```

## Executable Files
This problem is an extension of the previous problem in which we need to make /challenge/run executable and then execute it to get the flag
#### Method
- I use chmod u+x /challenge/run to get the current user execute permissions 
- I then execute /challenge/run and get the flag

```bash

```

## Permission Tweaking Practice
In this the user can cha get the permission using tools that are taught till present
#### Method
- I run the /challenge/run
- I change permissions using combinations of u,g,e,+,-,r,w,x

```bash

```

## Permissions Setting Practice
In this problem instead of adding or removing permissions we just set like chmod o=x /command
#### Method
- I run /challenge/run to start the challenge 
- I change permissions using some combinations of u,g,e,=,r,w,x 
- I run chmod u=rwx,g=rwx /flag and then cat /flag

```bash

```
## The SUID Bit
Some programs may be liked with SUID(set user id)Bits, which change the user to owner of the file, upon execution
#### Method

- I set a SUID ID by executing chmod u+s /challenge/get root
- I run /challenge/getroot opening 
- To get flag I run cat /flag
- 
```bash

```
