---
layout: post
title:  "Postman installation in Kali Linux"
author: sal
categories: [ Kali, DevOps ]
image: assets/images/postman4.png
beforetoc: "Installations on Debian OS always stands out differnet and here we have covered postman installation in kali linux"
toc: false
---

Postman is the Google chrome app for interacting with HTTP APIs. It give a user friendly interactive environment for creating request and reading responses.

Earlier, this app was an extension for the Google Chrome web browser. But as the popularity of this app increased, and more features were getting introduced in this application, its Google Chrome extension was deprecated for the Native desktop app.

If you are a debian user like us, then the below steps could help you with the installation,

1. Open the Terminal
2. Download Postman for Kali GNU/Linux 
3. Extract them to a temp directory,
    ```shell
    tar xvzf ~/Downloads/Postman*.tar.gz -C /tmp/
    ```
4. First setup super user as owner, 
    ```shell
    sudo chown -R root:root /tmp/Postman
    ```
5. Then relocate it,
    ```shell
    sudo mv /tmp/Postman /opt/
    ```
6. Make a symlink for easy launching on shell 
    ```shell
    sudo ln -s /opt/Postman/app/Postman /usr/local/bin/Postman
    ```

Finally start and enjoy Postman app in Kali Linux. From shell simply type in

![walking]({{ site.baseurl }}/assets/images/postman2.png)

![walking]({{ site.baseurl }}/assets/images/postman3.png)


Hope this information is helpful !!

