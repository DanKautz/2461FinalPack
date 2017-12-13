
Case Study: History of UNIX
A Brief History of Dragonfly BSD

Daniel E. Kautz
October 4, 2017

CSCI 2461-70
Computer Networking 3 - Linux
Week 6

Dragonfly BSD
This paper will present an overview of the history of the Unix-like operating system Dragonfly BSD from its initial development as a fork from the FreeBSD operating system in 2003 to its most recent release. This paper will summarize the background of Dragonfly’s development history, the reasoning behind beginning a fork from its predecessor system, and its initial release reception before presenting the highlights and major instances of its updates throughout the system’s history.
Dragonfly BSD began in June 2003 as a fork from the FreeBSD 4.8 operating system, under the development of Matthew Dillon, a FreeBSD developer since 1994, who announced the project a month later. [1] Dillon’s primary motivation for beginning this project was what he saw as suboptimal methods being used in the development of the next primary release, FreeBSD 5, in how that system would handle symmetric multiprocessing (SMP). Improving FreeBSD’s approach to multiprocessor application had been a significant element of development work on FreeBSD up to that point. [2] Dillon believed that development had taken a path that would lead to poor system performance and would be too complex to be maintainable, which led him to begin the Dragonfly project development using different methods to handle SMP. [3] The first release of Dragonfly BSD 1.0 followed a year later, on July 12, 2004, followed quickly by the 1.0A release on August 9, 2004 which cleaned up some initial critical bugs. This release was met with a response that considered it a “good start”. [4] Though the work done in the year since Dragonfly was announced was considered impressive, and its conceptual approaches contrasting with FreeBSD to the issues of SMP were not dismissed, the 1.0A release was not considered “stable” and was clearly not yet ready for wide production use. However, Dragonfly was considered to have wide potential if the development progress continued along the path already 
Footnotes
[1] “Announcing Dragonfly BSD!”, July 16, 2003, accessed September 20, 2017, https://lists.freebsd.org/pipermail/freebsd-current/2003-July/006889.html. 
[2] “Improving the FreeBSD SMP implementation”, published 2001, accessed September 20, 2017, http://www.lemis.com/grog/SMPng/USENIX/paper.pdf. 
[3] “Behind Dragonfly BSD”, Onlamp.com, July 8, 2004, accessed September 20, 2017, http://www.onlamp.com/pub/a/bsd/2004/07/08/dragonfly_bsd_interview.html. 
[4] “Dragonfly BSD 1.0A: A Strong Start”, Linux.com, August 9, 2004, accessed September 20, 2017, https://www.linux.com/news/dragonflybsd-10a-strong-start. 

shown in a year’s time. [5]
Development on the Dragonfly BSD system continued with regular releases of the 1.x family, beginning in April 2005 with 1.2 and continuing through 1.12 in April 2008. The primary focus of the 1.x development cycle was on rewriting most of the major kernel subsystems, which made the kernel more reliable and easily maintainable, and was intended as groundwork for the next phase of the project to support single system image clustering. [6] The 1.2 release, in April 2005, was much more stable than the 1.0A release and included a large number of bug fixes and performance improvements. 1.2 also made progress on the network subsystem, with the TCP stack being almost fully threaded. The 1.4 release in January 2006 saw the introduction of PKGSRC to manage third-party applications, meaning Dragonfly no longer supported the FreeBSD PORTS system. 1.6 in July 2006 included continued modifications to the kernel infrastructure, further increased stability over 1.4, and a major reorganization of the wireless framework of the system. The major feature of the 1.8 release, in January 2007, was the addition of virtual kernel support and a virtual kernel build target. 1.10, in August 2007, included a switch of the default ATA driver to NATA (a port from FreeBSD) and non-booting support for GPT partitioning and 64 bit disklabels. The 1.12 release, in February 2008, continued updates to the kernel and hardware systems and finished making libthread_xu the default threading library for the userland. [7]
The 2.x release family, extending from July 2008 to 2.10 in April 2011, began primarily focused on the release and improvement of the new HAMMER filesystem, intended to be the default filesystem used with Dragonfly BSD. HAMMER added many new capabilities to Dragonfly and served as the basis for the clustering work included in this second phase of the project. [8] Further development focused on SMP
Footnotes
[5] Linux.com, “Dragonfly BSD 1.0A: A Strong Start”.
[6] “History”, Dragonflybsd.org, last modified October 19, 2016, accessed September 20, 2017, https://www.dragonflybsd.org/history/. 
[7] “Releases”, Dragonflybsd.org, last modified August 8, 2017, accessed September 20, 2017, https://www.dragonflybsd.org/releases/. 
[8] Dragonflybsd.org, “History”.
scalability and developing new features. The 2.0 release, in July 2008, saw the first version of the HAMMER filesystem released and also included a great deal of work on wireless and Ethernet drivers. In the 2.2 release, from February 2009, HAMMER improvements continued, making it considered production-capable. Releases 2.6, 2.8, and 2.10, in April 2010, October 2010, and April 2011, further continued the improvements to HAMMER as well as continuing development of Dragonfly’s multiprocessor work. [9]
Among development focuses beginning in 2012 and included in the subsequent family of 3.x releases were work on bringing Dragonfly’s user-facing systems, including graphics and sound, up to the modern standards of other operating systems. [10] 3.0’s major features, released in February 2012, included major work on VM SMP scalability and improvements to HAMMER performance. 3.4, in April 2013, included performance improvements, a new USB stack, and a new default compiler, GCC 4.7. 3.4 also included an experimental packaging system, DPorts, which became the default in 3.6 in November 2013. The June 2014 release of 3.8 included the major work done on graphics drivers as well as the addition of dynamic binaries in the root filesystem. [11]
The current release family is the cycle of 4.x. Work in these developments has continued on SMP scalability as well as improving network performance. [12] 4.0 and 4.2, from November 2014 and June 2015, included further development on the graphics subsystem. 4.0 also ended support for 32-bit architecture, and 4.2 included the new GCC-5 base compiler and a new Dragonfly Mail Agent in the base system. Graphics support improvements continued with 4.4 and 4.6, in December 2015 and August 2016, and 4.6 also saw marked improvements over the previous standard of SMP performance. The most current release, initially 4.8 in March 2017 and updated with 4.8.1 on August 2, 2017, includes improved kernel performance and support for EFI as 
Footnotes
[9] Dragonflybsd.org, “Releases”.
[10] Dragonflybsd.org, “History”.
[11] Dragonflybsd.org, “Releases”.
[12] Dragonflybsd.org, “History”.

a mainstream boot environment. [13]
Dragonfly BSD has seen rapid and significant development since its beginning as a fork from the FreeBSD system in 2003. Through dedication to the initial vision of creating an alternative platform for the issues of symmetric multiprocessing, and continued work on improving the system’s kernel, hardware interaction, networking, the HAMMER filesystem, and desktop presentation, the developers have brought Dragonfly BSD far from its initial steps as an unstable and questionably necessary alternative to FreeBSD to a fully-featured, robust platform that continues to grow.












Footnotes
[13] Dragonflybsd.org, “Releases”.

References
“Announcing Dragonfly BSD!”, July 16, 2003, accessed September 20, 2017, https://lists.freebsd.org/pipermail/freebsd-current/2003-July/006889.html.
“Behind Dragonfly BSD”, Onlamp.com, July 8, 2004, accessed September 20, 2017, http://www.onlamp.com/pub/a/bsd/2004/07/08/dragonfly_bsd_interview.html. 
“Dragonfly BSD 1.0A: A Strong Start”, Linux.com, August 9, 2004, accessed September 20, 2017, https://www.linux.com/news/dragonflybsd-10a-strong-start. 
“History”, Dragonflybsd.org, last modified October 19, 2016, accessed September 20, 2017, https://www.dragonflybsd.org/history/. 
“Improving the FreeBSD SMP implementation”, published 2001, accessed September 20, 2017, http://www.lemis.com/grog/SMPng/USENIX/paper.pdf.
“Releases”, Dragonflybsd.org, last modified August 8, 2017, accessed September 20, 2017, https://www.dragonflybsd.org/releases/. 

