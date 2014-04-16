Server Scaling Capabilities using Socket Options
================================================

Kernel patch for enabling socket option (SO_REUSEPORT) in linux kernel version - 2.6.18-7.4. Support for both IPv4 and IPv6 sockets.

How to use?
===========

- Apply patch on kernel version 2.6.18-x.x  

How to enable?
==============

1. sysctl net.core.allow_reuseport=1 (Optional)
2. Before bind(), call setsockopt() with options SO_REUSEADDR and SO_REUSEPORT
3. Then the same as a normal socket - bind()/listen()/accept()

More Information
================

http://lwn.net/Articles/542629/

http://domsch.com/linux/lpc2010/Scaling_techniques_for_servers_with_high_connection%20rates.pdf

Thanks
Chris (srinivas.chandupatla@gmail.com)
