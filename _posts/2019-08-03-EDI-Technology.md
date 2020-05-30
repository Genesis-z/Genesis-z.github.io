---
layout: post
title:  "EDI Technology"
author: sal
categories: [ EDI ]
image: assets/images/EDI-1.png
beforetoc: "Introduction on the EDI technology, its importance in business and its usage"
toc: true
---

<!-- wp:paragraph -->
<p>

EDI (Electronic Data Interchange)&nbsp;is the transfer of data from one computer system to another by standardized message formatting, without the need for human intervention. It permits multiple companies from different countries to exchange documents electronically. It’s done through&nbsp;<a href="https://whatis.techtarget.com/definition/serial-communications-interface-SCI">serial links</a>&nbsp;and&nbsp;<a href="https://searchnetworking.techtarget.com/definition/peer-to-peer">peer-to-peer</a>&nbsp;networks, though most exchanges currently rely on the Internet for connectivity.<br></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>An EDI message contains a string of data elements, each of which would hold the information on purchase order, product model and many separated by delimiter. The entire string is called as data segment. One or more data segments wrapper within a header and a trailer segment forms the complete EDI data unit.<br>Both parties and the trading partners should be in the same page, have same set of rules on transmission. These standards define where and how the information from the document will be found. Translation software processes the information differently for sent and received messages and performs a complete audit of each step to ensure information is sent or received in EDI format.&nbsp;When the translator on the receiving computer reads a document, it knows where to find the buyer's company name, order number, purchase items and price, for example. This information is then sent to the receiver's order entry system without necessitating manual order entry.<br>EDI applies to documents such as purchase orders, invoices, shipping notices and commission sales reports, as well as other important or classified information. For an example, retailer can send the purchase orders to the suppliers in EDI exchange.</p>
<!-- /wp:paragraph -->

![EDI]({{ site.baseurl }}/assets/images/EDi2.jpg)

<!-- wp:paragraph -->
<p>Some major sets of EDI standards:<br></p>
<!-- /wp:paragraph -->

<!-- wp:list -->
<ul><li>The&nbsp;<a href="https://en.m.wikipedia.org/wiki/United_Nations">UN</a>-recommended&nbsp;<a href="https://en.m.wikipedia.org/wiki/UN/EDIFACT">UN/EDIFACT</a>&nbsp;is the only international standard and is predominant outside of North America.</li><li>The&nbsp;<a href="https://en.m.wikipedia.org/wiki/United_States">US</a>&nbsp;standard&nbsp;<a href="https://en.m.wikipedia.org/wiki/ASC_X12">ANSI ASC X12</a>&nbsp;(X12) is predominant in North America.</li><li><a href="https://en.m.wikipedia.org/wiki/GS1_EDI">GS1 EDI</a>&nbsp;set of standards developed the&nbsp;<a href="https://en.m.wikipedia.org/wiki/GS1">GS1</a>&nbsp;predominant in global&nbsp;<a href="https://en.m.wikipedia.org/wiki/Supply_chain">supply chain</a></li><li>The&nbsp;<a href="https://en.m.wikipedia.org/wiki/TRADACOMS">TRADACOMS</a>&nbsp;standard developed by the ANA (Article Number Association now known as&nbsp;<a href="https://en.m.wikipedia.org/w/index.php?title=GS1_UK&amp;action=edit&amp;redlink=1">GS1 UK</a>) is predominant in the&nbsp;<a href="https://en.m.wikipedia.org/wiki/United_Kingdom">UK</a>&nbsp;retail industry.</li><li>The ODETTE standard used within the European automotive industry</li><li>The VDA standard used within the European automotive industry mainly in Germany</li><li><a href="https://en.m.wikipedia.org/wiki/HL7_Services_Aware_Interoperability_Framework">HL7</a>, a semantic interoperability standard used for healthcare data.</li><li><a href="https://en.m.wikipedia.org/wiki/Health_Insurance_Portability_and_Accountability_Act">HIPAA</a>, The Health Insurance Portability and Accountability ACT (HIPAA), requires millions of healthcare entities who electronically transmit data to use EDI in a standard HIPAA format.</li><li><a href="https://en.m.wikipedia.org/w/index.php?title=IATA_Cargo-IMP&amp;action=edit&amp;redlink=1">IATA Cargo-IMP</a>, IATA Cargo-IMP stands for International Air Transport Association Cargo Interchange Message Procedures. It’s an EDI standard based on EDIFACT created to automate and standardize data exchange between airlines and other parties.</li><li><a href="https://en.m.wikipedia.org/wiki/NCPDP_SCRIPT">NCPDP Script</a>, SCRIPT is a standard developed and maintained by the National Council for Prescription Drug Programs (NCPDP). The standard defines documents for electronic transmission of medical prescriptions in the United States.</li><li>Edig@s (EDIGAS) is a standard dealing with commerce, transport (via pipeline or container) and storage of gas.</li><li>Many of these standards first appeared in the early to mid 1980s. The standards prescribe the formats, character sets, and data elements used in the exchange of business documents and form</li></ul>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p>Some of standard EDI data keywords would be like ORDER (Eancom order), ORDHDR (Tradacom order), INVOIC (Eancom invoice), INVFIL (Tradacom invoice), DESADV (Advance shipping notice), TUN (Tradanet user number&nbsp;–&nbsp;defines trading relationship between trading partners, SNRF ( sender reference number&nbsp;–&nbsp;an identification number for each data sent or received).<br>Explore more on&nbsp;<a href="https://www.edibasics.co.uk/edi-resources/glossary/">EDI basics</a>&nbsp;here.<br>Automating paper-based tasks improves data quality, and transactions are exchanged within seconds or minutes instead of days or weeks. EDI frees up staff time to work on more important tasks. Business-critical data is sent on time and tracked in real time by automating the transfer of data among applications across a supply chain. The system is expensive to implement and usually requires help from a consultant that specializes in the field.<br>EDI can be transmitted using any methodology agreed to by the sender and recipient, like FTP (File transfer Protocol), SFTP ( same as FTP but use secure shell protocol), HTTP,&nbsp;&nbsp;<a href="https://en.m.wikipedia.org/wiki/AS1_%28networking%29">AS1&nbsp;</a>(based on SMTP and S/MIME)&nbsp;,&nbsp;<a href="https://en.m.wikipedia.org/wiki/AS2">AS2&nbsp;</a>,&nbsp;<a href="https://en.m.wikipedia.org/wiki/AS4">AS4&nbsp;</a>and many.<a href="https://en.m.wikipedia.org/wiki/AS4"></a><br>A sample EDI documents looks like,<br></p>
<!-- /wp:paragraph -->

![EDI]({{ site.baseurl }}/assets/images/EDI3.png)

Hope this article gives idea on the EDI technology, its data and its usage in business.

Please share your comments below !!
