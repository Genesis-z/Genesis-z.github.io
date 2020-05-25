---
layout: post
title:  "Cryptojacking Worm - in Docker Containers"
author: sal
categories: [ Docker, DevOps ]
image: assets/images/crypto-docker-attack.png
beforetoc: "A worm attack in Docker container"
toc: false
featured: true
---

A new [cryptojacking worm](https://www.malwarebytes.com/cryptojacking/), named Graboid, has been spread into more than 2,000 Docker hosts, according to the [Unit 42](https://unit42.paloaltonetworks.com/) researchers from Palo Alto Networks. This is the first time such a piece of malware has spread via containers within the Docker Engine (specifically docker-ce).

This is because most of the end point software does  not inspect data and activities inside containers, this type of malicious activity can be difficult to detect. It all started through  unsecured [Docker](https://docs.docker.com/engine/api/v1.24/) daemons, where a Docker image was first installed to run on the compromised host. The malware, which was downloaded from command and control (C2) servers, is deployed to mine for [Monero](https://www.getmonero.org/) and periodically queries for new vulnerable hosts from the C2 and picks the next target at random to spread the worm to. The Docker team worked quickly in tandem with Unit 42 to remove the malicious images once our team alerted them of this operation.


![walking]({{ site.baseurl }}/assets/images/Cryptojacking-worm-activity-overview.png)

Graboid malware (the cryptojacking worm) is capable of, 

1. Cryptomining
2. Spreading to other vulnerable hosts

How it works looks something like this:

- That hacker locates an insecure Docker host and sends remote commands to download and deploy a malicious image named `pocosow/centos:7.6.1810.`
- Using a malicious script (`/var/sbin/bash`) within the container, four shell scripts (`live.sh, worm.sh, cleanxmr.sh, and xmr.sh`) are downloaded from a Command and Control (C2) server.

The four scripts are executed, one at a time, with the following purposes:

- The `live.sh` sends the number of available CPUs to the compromised C2 server.
- The `worm.sh` script downloads a file that contains a list of IP addresses of hosts with unsecured Docker API endpoints and then randomly chooses one of the addresses as its target to deploy the infected container.
- The `cleanxmr.sh` script randomly picks one of the hosts from the list and stops the cryptojacking containers on the target.
- The `xmr.sh` randomly picks one of the hosts and deploys another image (gakeaws/nginx), which contains a binary masquerading as nginx.

With regards to Graboid, Hatch says, 

> “Not only can the Graboid vulnerability spread, but the attack vector it uses is one of the oldest attack vectors out there. It is a simple software delivery hijack.” 

In other words, what would normally be a simple means of spreading and detecting, has been made exponentially more challenging (on the detecting side of things) due to the attacker using containers.

## Conclusion:

Anti virus and anti-malware applications have no way of analyzing and cleaning containers & Container images. This is the major problem, even tools like  Harbor are only capable of determining if an image contains a vulnerability (not fixing them).  

Because of this we have to use only trusted images and secure API servers for the likes for Dockers and Kubernetes. As a container administrator, we need to completely understand the tools available and the best practice's for the tools we use