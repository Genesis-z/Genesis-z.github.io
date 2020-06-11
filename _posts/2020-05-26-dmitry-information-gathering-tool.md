---
layout: post
title:  "Dmitry - Information Gathering Tool"
author: john
categories: [ Kali ]
comments: True
image: assets/images/tech.jpeg
beforetoc: "An Overview about Dmitry tool"
toc: false
---
Networking got bunch of advanced information gathering tools like nmap. But yet dmitry satisfies some criteria that forms foundation of information gathering.

Being a light weighted tool, dmitry tool is able to perform a bunch of operations like 'whois' lookups, fetching netcraft information, scanning for open TCP  in a host etc.

So lets dive into deep magic...

> Dmitry tool is programmed James Greig. It is written in C language

To the crisp, dmitry is well known `passive information gathering tool`. Which means information are gathered without any connection between the penetration tester and the target.

The commands were simple. 

![DmitryShell]({{ site.baseurl }}/assets/images/dmitry.png)

```shell
dmitry -i 216.239.34.117
```

The `-i` command would perform a `whois lookup` with IP address input. The whois command would fetch data regarding domain name, registrar URL, contact email, license expiry etc.

```shell
dmitry -w google.com
```

The `-w` command performs same whois lookup with domain name as input. 

```shell
dmitry -n google.com
```

The `-n` performs fetching of netcraft related information on a host. 

Likewise, `-s` retrieves all subdomains registered under the host(Try with google.com for a clear picture on this).

`-e` retrieves the available email id's registered under the host.

`-p` performs a TCP port scan and lists all available port counts.

`-f` would give the filtered port information. It simply means information about TCP ports that are blocked by some firewall or some other obstacle and hence the tool cannot determine whether those ports are opened or closed. This needs to be passed along with -p input. Nevertheless, dmitry by default considers -p if it is not mentioned.

Similar to `-f`, `- b` needs to be mentioned with -p port scan command. 

```shell
dmitry -pb google.com
```

This would read the banner information of the host. In general, banner denotes the information about a service running. For instance like version information. It is also used to retrieve information about the remote servers running on a host and also peek about services running on open TCP ports.

The `-t` flag enables the pen-tester to configure the TTL value as per their need.

Finally is `-o` flag. This catches the output to a file.

```shell
dmitry -wo file.txt google.com
```

The above command would perform a whois lookup on google.com and writes the output data into 'file.txt'. We can either open the file or read it on terminal with a cat command. By default all results are displayed in terminal. To read the output file in terminal itself use below command,

```shell
cat file.txt
```

Remember after `-o` flag always the file name need to be mentioned, not the host information.

Moreover, multiple flags can be combined in a single command and the behavior would just be the same.

```shell
dmitry -wpseo scan.txt google.com
```

The above command would perform a whois lookup on google.com and fetches the subdomain information available, any email registered under the host domain and writes all these outputs in a file named 'scan.txt'. The file will be saved in the root folder.

So this is something about dmitry tool.
If you find this post useful, please share this knowledge with everyone.

[Let be there some deep magic going on!!!](https://tools.kali.org/information-gathering/dmitry)