# SYSNET

[![Build Status](https://travis-ci.org/matteyeux/sysnet.svg?branch=master)](https://travis-ci.org/matteyeux/sysnet)
[![Platform](https://img.shields.io/badge/platform-multiples-yellowgreen.svg)](https://github.com/matteyeux/sysnet#platforms-tested-) 
[![Packagist](https://img.shields.io/badge/license-MIT-orange.svg)](https://github.com/matteyeux/sysnet/blob/master/LICENSE)&nbsp;
[![Packagist](https://img.shields.io/badge/contact-matteyeux-blue.svg)](https://twitter.com/matteyeux) 

```
Usage : sysnet [OPTIONS]
 -s, --system	system information
 -n, --network	network information
 -c, --cpu	cpu information
 -d, --disk	disk information
 -a, --all	all information
 -v, --version	version
```

Sysnet is a tool which grabs system & network information.
This tool supports Linux, OS X, & [iOS](https://github.com/theos/theos)

###  System 

```
User : 			mathieu
Operating System :	Linux
version :		3.16.0-4-amd64
architecture : 		x86_64
n° of processes : 	225
shell : 		/bin/bash

Used RAM : 		0.74 GB
Free RAM : 		3.12 GB
Total RAM : 	3.86 GB

```

### Network

```
hostname: pwn
lo
	address: 127.0.0.1
	netmask: 255.0.0.0		suffix : 8
eth0
	address: 192.168.181.128
	netmask: 255.255.255.0		suffix : 24
	broadcast: 192.168.181.255
IPv6 lo
	address: ::1
IPv6 eth0
	address: fe80::20c:29ff:feb0:ddf5%eth0

Gateway : 192.168.181.2
```

### Disk 
I also added support for disk information :

```
$ ./sysnet -d /
Disk usage of / : 	7.10 GB
Free space in / : 	30.50 GB
Total in /: 		37.60 GB
```

### CPU 
I am currently improving sysnet by supporting CPU information using [libcpuid](https://github.com/matteyeux/libcpuid)

```
$ ./sysnet -c
Vendor :		GenuineIntel
Model :			Intel(R) Core(TM) i5-6200U CPU @ 2.30GHz
Physical cores :	2
```

### Demo

Here is an obsolete demo of sysnet running on GNU/Linux Debian 8.5. 

[![sysnet demo](https://asciinema.org/a/6jo8dd7d66ljrso5xon8ob5ub.png)](https://asciinema.org/a/6jo8dd7d66ljrso5xon8ob5ub)

### Platforms tested :

- Linux
- macOS
- iOS 9

### TODO

The TODO list is [here](https://github.com/matteyeux/sysnet/projects/1)

### Installation 

Since v1.1.1 sysnet needs [libcpuid](https://github.com/matteyeux/libcpuid) to be built.
Make sure you have GCC installed

By default, the install directory is `/usr/bin/`, you can change it by modifying `INSTALL_DIR` variable in the [Makefile](https://github.com/matteyeux/sysnet/blob/master/Makefile#L4) 

You can now cross-compile sysnet for Raspberry Pi and also build and `.deb` to install it. 
Make sure to have the toolchain setup in your $PATH.

### Credits

Tool developed by [@matteyeux](https://twitter.com/matteyeux)
