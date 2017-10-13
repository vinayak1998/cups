---
title: How To Restrict Printer Information Being Sent Out From A Server
layout: post
permalink: /blog/:year-:month-:day-:title.html
---

Printer browsing allows your server to automatically share its printers with client machines and other servers. To make sure that this printer information is sent to the right computers, edit the /etc/cups/cupsd.conf file. Locate the BrowseAddress directive and then edit or add IP or netmask addresses to your liking. Some examples:

 # Broadcasts to all computers through all interfaces
 
 BrowseAddress 255.255.255.255:631
 
 # Broadcast to all computers on the 192.0.2.x network
 
 BrowseAddress 192.0.2.255:631
 
 # Broadcast to computers 192.0.2.14 and 192.0.2.15
 
 BrowseAddress 192.0.2.14:631
 BrowseAddress 192.0.2.15:631
 
 # Specific hostname address (must enable HostNameLookups)
 
 BrowseAddress host.domain.com:631
