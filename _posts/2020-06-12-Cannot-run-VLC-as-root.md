---
layout: post
title:  "Troubleshoot-Cannot run VLC as root"
author: john
categories: [ Kali ]
comments: True
image: assets/images/casette.jpeg
beforetoc: "Solution for Vlc issue"
toc: false
---

After fresh installation or upgrade of existing versions, Vlc might not open. On trying the best with terminal, if you have received traces like `Cannot run vlc as root` this post could solve your problem.

Fire up your terminal.

Navigate to the path `/usr/bin/vlc```. This is the binary file of vlc.

To read the binary, provide below command in terminal

```shell
hexeditor /usr/bin/vlc
```
or if you are already in that path, just 

```shell
hexeditor vlc
```

This will open up the binary file with hexeditor interface.

Press `Ctrl+W`. And choose `search for text string` in the pop up. This enables us to search for any text in the file.

Input string `geteuid` and press enter. After the result is fetched, press `Tab key`. This would toggle the cursor to next column in hexeditor.

Replace `geteuid` text as `getppid`.

![Vlctroubleshoot]({{ site.baseurl }}/assets/images/vlc.png)

Press `Ctrl+X` to save. Filename should be `vlc` or `/usr/bin/vlc`.

Process is done. Now fireup Vlc and have fun!.
