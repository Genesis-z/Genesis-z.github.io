---
layout: post
title:  "Docker Machine & Docker Engine"
author: sal
categories: [ Docker, DevOps ]
image: assets/images/Docker-machine-1.jpg
beforetoc: " A step by step process to create your first project with Django"
toc: false
---

<!-- wp:paragraph -->
<p><strong>What is Docker Machine?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Docker Machine is a tool that lets you install Docker Engine
on virtual hosts, and manage the hosts with&nbsp;docker-machine&nbsp;commands. You can use Machine to create Docker hosts on
your local Mac or Windows box, on your company network, in your data center, or
on cloud providers like Azure, AWS, or DigitalOcean.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Using&nbsp;docker-machine&nbsp;commands, you can start, inspect,
stop, and restart a managed host, upgrade the Docker client and daemon, and
configure a Docker client to talk to your host.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Example: </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>docker-machine env default&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li>Run the above command to point to a host called default.</li><li>Follow on the screen instructions to complete the <strong>env </strong>setup </li><li>Run the docker commands like <strong>docker ps,</strong> docker&nbsp; run hello-world      and so forth</li></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p><strong>Why should I use it?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Docker Machine enables you to provision multiple remote Docker hosts on various flavors of Linux. Additionally, Machine allows you to run Docker on older Mac or Windows systems, as described in the previous topic. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Docker Machine has these two broad use cases.</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li><strong>I have an      older desktop system and want to run Docker on Mac or Windows</strong></li></ul>
<!-- /wp:list -->

![Docker_machine]({{ site.baseurl }}/assets/images/Docker-machine-2.png)

<!-- wp:paragraph -->
<p>If you work primarily on an older Mac or Windows laptop or
desktop that doesn’t meet the requirements for the new&nbsp;<a href="https://docs.docker.com/docker-for-mac/">Docker
Desktop for Mac</a>&nbsp;and&nbsp;<a href="https://docs.docker.com/docker-for-windows/">Docker Desktop for Windows</a>&nbsp;apps, then you need Docker Machine to run Docker Engine
locally. Installing Docker Machine on a Mac or Windows box with the&nbsp;<a href="https://docs.docker.com/toolbox/overview/">Docker
Toolbox</a>&nbsp;installer
provisions a local virtual machine with Docker Engine, gives you the ability to
connect it, and run&nbsp;docker&nbsp;commands.</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li><strong>I want to provision Docker hosts on remote systems</strong></li></ul>
<!-- /wp:list -->

![Docker_machine]({{ site.baseurl }}/assets/images/Docker-machine-3.png)

<!-- wp:paragraph -->
<p><strong>Docker Engine</strong> runs natively on Linux systems. If you have a Linux box as your primary system, and want to run&nbsp;docker&nbsp;commands, all you need to do is download and install Docker Engine. However, if you want an efficient way to provision multiple Docker hosts on a network, in the cloud or even locally, you need Docker Machine. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Whether your primary system is Mac, Windows, or Linux, you can install Docker Machine on it and use&nbsp;docker-machine&nbsp;commands to provision and manage large numbers of Docker hosts. It automatically creates hosts, installs Docker Engine on them, then configures the&nbsp;docker&nbsp;clients. Each managed host (“<strong><em>machine</em></strong>”) is the combination of a Docker host and a configured client.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>What’s the difference between Docker Engine and Docker Machine?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>When people say “Docker” they typically mean&nbsp;<strong>Docker Engine</strong>, the client-server application made up
of the Docker daemon, a REST API that specifies interfaces for interacting with
the daemon, and a command line interface (CLI) client that talks to the daemon
(through the REST API wrapper). Docker Engine accepts&nbsp;docker&nbsp;commands from the CLI, such as&nbsp;docker run &lt;image&gt;,&nbsp;docker ps&nbsp;to
list running containers,&nbsp;docker image ls&nbsp;to
list images, and so on.</p>
<!-- /wp:paragraph -->

![Docker_machine]({{ site.baseurl }}/assets/images/Docker-machine-4.png)

<!-- wp:paragraph -->
<p><strong>Docker Machine</strong>&nbsp;is
a tool for provisioning and managing your Dockerized hosts (hosts with Docker
Engine on them). Typically, you install Docker Machine on your local system.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Command line information:</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li>Docker Machine - docker-machine is the CLI</li><li>Docker Engine  - docker is the Command line interface </li></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>You can use Machine to install Docker Engine on one or more virtual
systems. These virtual systems can be local (as when you use Machine to install
and run Docker Engine in VirtualBox on Mac or Windows) or remote (as when you
use Machine to provision Dockerized hosts on cloud providers). The Dockerized
hosts themselves can be thought of, and are sometimes referred to as, managed
“machines”.</p>
<!-- /wp:paragraph -->

![Docker_machine]({{ site.baseurl }}/assets/images/Docker-machine-5.png)

