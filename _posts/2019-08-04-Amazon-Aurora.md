---
layout: post
title:  "Amazon Aurora"
author: sal
categories: [ AWS, DevOps ]
image: assets/images/Database.jpg
beforetoc: "A simple article about Amazon aurora DB"
toc: false
---

Amazon Aurora is a MySQL-compatible relational database engine  that combines the speed and availability of high-end commercial databases with the simplicity and cost-effectiveness of open-source databases. Amazon Aurora provides up to five times better performance than MySQL with the security, availability, and reliability of a commercial database at one tenth the cost. 

<!-- wp:paragraph -->
<p><strong>Benefits of Amazon Aurora</strong></p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li> Fully managed&nbsp;– Amazon Aurora is a fully managed database service.&nbsp;&nbsp;There is no need to worry about database management tasks such as hardware provisioning, software patching, setup, configuration, monitoring, or backups. Amazon Aurora automatically and continuously monitors and backs up your database to Amazon Simple Storage Service (Amazon S3), enabling granular point-in-time recovery </li><li> Highly available and durable&nbsp;– When you run your SAP Hubris Commerce system on Amazon Aurora, you can take advantage of Amazon Aurora’s high availability features. Amazon Aurora is designed to offer greater than 99.99% availability. </li></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Recovery from physical storage failures is transparent, and instance fail over typically requires less than&nbsp;30 seconds.&nbsp;Amazon Aurora’s storage is fault-tolerant and self-healing.&nbsp;Six copies of your data are replicated &nbsp;across
three Availability Zones and continuously backed up to Amazon S3.</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li> High performance&nbsp;– Amazon Aurora provides five times the throughput of standard MySQL or twice the throughput of standard PostgreSQL running on the same hardware. </li><li> Highly scalable&nbsp;– You can scale your Amazon Aurora database from an instance with 2 vCPUs and 4 GiB of memory up to an instance with 32 vCPUs and 244 GiB of memory. You can also add up to 15 low-latency read replicas across three Availability Zones to further scale read capacity. Amazon Aurora automatically grows storage as needed, from 10 GiB up to 64 TiB </li><li> Highly secure&nbsp;– Amazon Aurora provides multiple levels of security for your database. These include network isolation using Amazon Virtual Private Cloud (Amazon VPC), encryption at rest using keys you create and control through AWS Key Management Service (AWS KMS), and encryption of data in transit using Secure Sockets Layer (SSL). On an encrypted Amazon Aurora instance, data in the underlying storage is encrypted, as are the automated backups, snapshots, and replicas in the same cluster. </li></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p><strong>&nbsp;Instant Crash recovery:</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>&nbsp;Amazon Aurora is designed to recover from a crash almost instantaneously and continue to serve your  application data. Unlike other databases, after a crash Amazon Aurora does not need to replay the redo-log  from the last database checkpoint before making the database available for operations. Amazon Aurora&nbsp;performs
crash recovery asynchronously on parallel threads, so your database is open and
available&nbsp;immediately
after a crash.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Because
the storage is organized in many small segments, each with its own redo log,
the underlying&nbsp;storage
can replay redo records on demand in parallel and asynchronously as part of a
disk read after a&nbsp;crash.
This approach reduces&nbsp;&nbsp;database restart times to less than 60 seconds
in most cases.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Survivable Caches</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In Amazon Aurora, the database buffer cache has been moved out of the database process. If a database&nbsp;restarts, the cache remains warm, and performance is not impacted due to a cold cache as is the case with traditional
databases. This approach lets you resume fully loaded operations much faster.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>( Note:&nbsp;<a href="http://www.exploreoracle.com/2009/03/31/database-buffer-cache/">Database
Buffer</a>&nbsp;Cache is the place where data blocks
are copied from data files to perform SQL&nbsp;operations.
Buffer Cache is shared memory structure and it is concurrently accessed by all
server processes)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>There
are lot more benefits other than the above mentioned,</p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li>speed</li><li>Scalability</li><li>Increased availability</li><li>Reduced cost</li><li>Improved Customer Experience</li><li>Reduced administration</li></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>You can create free&nbsp;<a href="https://portal.aws.amazon.com/billing/signup?redirect_url=https%3A%2F%2Faws.amazon.com%2Fregistration-confirmation#/start">Aurora
account</a>&nbsp;and explore more in compatible
relational Database.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Hope
this would have given some idea on Amazon Aurora. Please like and share your
thoughts in the&nbsp;comment
below</p>
<!-- /wp:paragraph -->