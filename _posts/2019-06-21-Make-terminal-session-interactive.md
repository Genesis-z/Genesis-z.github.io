---
layout: post
title:  "Make your terminal sessions interactive"
author: sal
categories: [ Linux, tips & tricks ]
image: assets/images/terminal.jpg
beforetoc: "The simple tools to make the terminal scripts more user interactive"
toc: false
featured: true
---

Sometimes,working with the terminals black & white screen is little boring. Creating new interactive dialog/interactive boxes in our terminal will be little fun and interesting. Here I brought some tools to make the terminal sessions interesting,nteractive dialog boxes in our termial,

1. dialog
2. whiptail
3. zenity

### Dialog

It allows us to create interactive screens to make the regular task interesting. you can follow the below to install the dialog command line utility. 

For debian/ubuntu users,

```shell
sudo apt-get update
sudo apt-get install dialog
```

CentOS / Redhat users

```shell
yum install dialog
```

Here is a simple example to turn a regular script with interactive screens,

> before using dialog -- Normal shell script

<p><script src="https://gist.github.com/Dimension8d/5ff0b25296d19e65efc1dbc0c3fe6748.js"></script></p>

![termial]({{ site.baseurl }}/assets/images/terminal1_dialog.png)

<!-- ![termial]({{ site.baseurl }}/assets/images/terminal2_dialog.png) -->

![termial]({{ site.baseurl }}/assets/images/terminal3_dialog.png) 

> After using dialog

<p><script src="https://gist.github.com/Dimension8d/8ae044e45298a174d2e7b6b41a96a10f.js"></script></p>

![termial]({{ site.baseurl }}/assets/images/termianl_withdialog.png)

![termial]({{ site.baseurl }}/assets/images/termial2_withdialog.png)

![termial]({{ site.baseurl }}/assets/images/termianl3_withdialog.png) 

Find more information on the [here](https://bash.cyberciti.biz/guide/Bash_display_dialog_boxes#:~:text=The%20dialog%20command%20allows%20you,TTY%20(terminal)%20dialog%20boxes.)


### Whiptail

It is a program which allow us to display dialog boxes to the user informational purposes or to get the input from the user.

Here is a simple example on how whiptail works,

```
whiptail --title "Menu example" --menu "Choose an option" 25 78 16 \
"<-- Back" "Return to the main menu." \
"Add User" "Add a user to the system." \
"Modify User" "Modify an existing user." \
"List Users" "List all users on the system." \
"Add Group" "Add a user group to the system." \
"Modify Group" "Modify a group and its list of members." \
"List Groups" "List all groups on the system."
```
![Whiptail]({{ site.baseurl }}/assets/images/whiptail.png)

Find more on the whiptail [wikibook](https://en.wikibooks.org/wiki/Bash_Shell_Scripting/Whiptail) here

### Zenity:

This is also a wonderful tool which displays  GTK+ Dialog Boxes in command line and using shell script. Its speciality is that it allows us  to create graphical dialog boxes in th command line to make the interaction between the user and the shell very easy.

Find more on [zenity](https://linuxconfig.org/how-to-use-graphical-widgets-in-bash-scripts-with-zenity) here ...

Among these, my personal favourite is `dialog` and `whiptail`. Please share your experience with anyother tool other than this, in the comment below.






