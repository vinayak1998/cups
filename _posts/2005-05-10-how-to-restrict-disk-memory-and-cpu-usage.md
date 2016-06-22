---
title: How To Restrict Disk, Memory and CPU Usage
layout: post
permalink: /blog/:year-:month-:day-:title.html
---

If you are running into a performance problem with disk space, memory and CPU usage, editing one or more of the following directives inside the /etc/cups/cupsd.conf file may aid the situation.

 /etc/software/init.d/cups stop ENTER
 rm -f /var/spool/cups/c* ENTER
 rm -f /var/spool/cups/tmp/* ENTER
 /etc/software/init.d/cups start ENTER