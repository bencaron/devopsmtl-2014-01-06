# Installation

Starting from a 12.04 Ubuntu image:

Install python-software-properties (for 12.04):

```bash
root@vagrant:~# apt-get install -y python-software-properties
Reading package lists... Done
Building dependency tree
Reading state information... Done
The following extra packages will be installed:
  python-pycurl
Suggested packages:
  libcurl4-gnutls-dev python-pycurl-dbg
The following NEW packages will be installed:
  python-pycurl python-software-properties
0 upgraded, 2 newly installed, 0 to remove and 137 not upgraded.
Need to get 23.8 kB/73.0 kB of archives.
After this operation, 428 kB of additional disk space will be used.
Get:1 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main python-software-properties all 0.82.7.6 [23.8 kB]
Fetched 23.8 kB in 0s (111 kB/s)
Selecting previously unselected package python-pycurl.
(Reading database ... 60857 files and directories currently installed.)
Unpacking python-pycurl (from .../python-pycurl_7.19.0-4ubuntu3_amd64.deb) ...
Selecting previously unselected package python-software-properties.
Unpacking python-software-properties (from .../python-software-properties_0.82.7.6_all.deb) ...
Processing triggers for man-db ...
Setting up python-pycurl (7.19.0-4ubuntu3) ...
Setting up python-software-properties (0.82.7.6) ...
```

## Install Dokku itself

```bash
wget -qO- https://raw.github.com/progrium/dokku/v0.2.1/bootstrap.sh | sudo DOKKU_TAG=v0.2.1 bash
```

