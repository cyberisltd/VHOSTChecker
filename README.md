VHOSTChecker
============

* Author: geoff.jones@cyberis.co.uk
* Copyright: Cyberis Limited 2013
* License: GPLv3 (See LICENSE)

A Perl script to enumerate hidden VHOSTS on a remote webserver.

The script will show the differing responses between requests, and the length of each, allowing you to quickly identify vhosts of interest, regardless of whether there is an associated DNS entry. If you find something, just be sure to create a static host entry before viewing in a browser!

Usage
-----
```
/vhostchecker.pl -i ips.txt -h hosts.txt --append .cyberis.co.uk
[INFO] Read 1 IP's from file "ips.txt" 
[INFO] Read 18 vhosts from file "hosts.txt" 

Checking IP: 95.142.175.1 [C:301 L:233 R:http://www.cyberis.co.uk/]
Checking VHOST against 95.142.175.1: staging.cyberis.co.uk [C:301 L:233 R:http://www.cyberis.co.uk/]
Checking VHOST against 95.142.175.1: prelive.cyberis.co.uk [C:301 L:233 R:http://www.cyberis.co.uk/]
Checking VHOST against 95.142.175.1: pre-live.cyberis.co.uk [C:301 L:233 R:http://www.cyberis.co.uk/]
Checking VHOST against 95.142.175.1: test.cyberis.co.uk [C:301 L:233 R:http://www.cyberis.co.uk/]
Checking VHOST against 95.142.175.1: www.cyberis.co.uk [C:200 L:14496]
```
Dependencies
------------
Perl, and the following modules:
```perl
use Getopt::Long;
use Term::ANSIColor;
require LWP::UserAgent;
require LWP::Protocol::https;
```

Issues
------
Kindly report all issues via https://github.com/cyberisltd/VHOSTChecker/issues
