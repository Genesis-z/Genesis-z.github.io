---
layout: post
title:  "The Sudoers - Controlling privileages"
author: john
categories: [ Linux , tips & tricks ]
comments: True
image: assets/images/sudo.jpg
beforetoc: "Understanding Sudoers file"
toc: false
featured: true
---

Sudoers is a file in directory '/etc/sudoers' in Linux or Mac OS. By editing this file, we can control the access granted to various clients.

We all are familiar that `root` user in linux has elevated privileages i.e execute anything in linux. And a normal user has no such advantages unless provided.

Conventionally, linux is built with `security purpose` in mind. Hence while any user tries to execute something, system will compare the username with the sudoers file. If the user is not available in the provided list, then permission would get denied.

## Purpose of Sudoers

By editing Sudoers file, you can grant a user/group with privileaged user access, block a user/group with certain limits, create aliasing etc.
By default, sudoers need to be opened with command 
```shell 
visudo
``` 
this opens sudoers file in vi editor. Vi editor is to prevent any accidental modifications of existing file with an unknown or erroneous syntax. If sudoers file is modified with any wrong syntax, it may lock all users and the recovery could be quite tedious.

## Sudoers file

By default vi will open in command mode. To edit the file press 'i' (INSERT) and edit as per the need. Lines with `~` in sudoers file denotes empty lines. Comments in sudoers are denoted with '#'s. 

* The first command of the file contains Defaults,
`Defaults env_reset` This clears the env variables to default value in order to block any harmful environment variables created by other users. 
`Defaults mailbadpass`, will notice the incorrect password attempts done with sudo to the configured mail id in root user profile. 
`Defaults secure path`, contains the $PATH or in other terms environment variable. 

* Next command is `root ALL=(ALL:ALL) ALL`. This configures access levels to various users.
`root` denotes the user name. First `ALL` refers to the hosts. Suppose there are some 10 hosts connected to your network and you want hosts 'sample1' and 'sample2' alone have some privileaged access, those host name need to be mentioned here. 

```shell
root sample1 sample2 = (ALL:ALL) ALL
```

* The second and third 'ALL' in `(ALL:ALL)` denotes the user, groups respectively i.e User 'root' can execute the commands as all users/groups(by default- root, or any user/gruops configured in ~bashrc). The final `ALL` denotes command lists. If we want to limit execution of command lists for a user, those commands need to be mentioned here.

* Next line would start with a `'*%'-'sudo'`. This denotes that 'sudo' is a group. Rest of the commands has same syntax as explained above.

* Final line would be '#includedir'. Though it starts with an asterick and should mean as comment, it is actually an include statement just like in c/c++ programs. Any additional modification or list of configurations can be made seperately in /etc/sudoers.d file. This will get linked to sudoers file with `#includedir`.

## Aliasing

The next glancing would be on 'Aliasing' in sudoers file. In a default sudoers, there are three aliasing commented out. Host aliasing, User aliasing and Command aliasing. In simple terms, aliasing is grouping down.

For instance, we have some 5 users, whom should have particular privileages and remaining should have different set of privileages. 
This can be done as 
```shell
User_Alias GROUPA = sample1, sample2
User_Alias GROUPB = sample3, sample1
```
Here, we have grouped users in two. We can mention the groupname instead of mentioning all users in our further commands. Please note that the name should be in CAPITAL letters.

```shell
GROUPA ALL = (ALL:ALL) /sbin/shutdown
```
In same way we can bring down hosts and commands under groups.

```shell
Cmnd_Alias POWEROPTIONS = /sbin/shutdown, /sbin/reboot, /sbin/restart
GROUPB ALL = POWEROPTIONS
```
Here we have grouped power related commands under POWEROPTIONS and provide GROUPB to have rights on executing power related commands.

## To summarize...

These configurations can be edited as per one's need. If you are the SINGLE user of your system, most probably there would be no need of configuring this file. But in case of multi users or for administrative purpose, this comes in hand.

Hope this post shared some useful information!!!