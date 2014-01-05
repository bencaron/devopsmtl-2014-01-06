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

And the looooooong list of stuff it does (about 5 minutes on a decent connection):

Chef folks will say it's not idempotent enough ;) (double-triple apt-get update for exemple)

```bash
root@vagrant:~# wget -qO- https://raw.github.com/progrium/dokku/v0.2.1/bootstrap.sh | sudo DOKKU_TAG=v0.2.1 bash
Ign http://us.archive.ubuntu.com precise InRelease
Ign http://us.archive.ubuntu.com precise-updates InRelease
Ign http://us.archive.ubuntu.com precise-backports InRelease
Ign http://security.ubuntu.com precise-security InRelease
Hit http://us.archive.ubuntu.com precise Release.gpg
Hit http://us.archive.ubuntu.com precise-updates Release.gpg
Hit http://security.ubuntu.com precise-security Release.gpg
Hit http://us.archive.ubuntu.com precise-backports Release.gpg
Hit http://us.archive.ubuntu.com precise Release
Hit http://security.ubuntu.com precise-security Release
Hit http://us.archive.ubuntu.com precise-updates Release
Hit http://security.ubuntu.com precise-security/main Sources
Hit http://us.archive.ubuntu.com precise-backports Release
Hit http://us.archive.ubuntu.com precise/main Sources
Hit http://us.archive.ubuntu.com precise/restricted Sources
Hit http://us.archive.ubuntu.com precise/universe Sources
Hit http://us.archive.ubuntu.com precise/multiverse Sources
Hit http://us.archive.ubuntu.com precise/main amd64 Packages
Hit http://us.archive.ubuntu.com precise/restricted amd64 Packages
Hit http://us.archive.ubuntu.com precise/universe amd64 Packages
Hit http://us.archive.ubuntu.com precise/multiverse amd64 Packages
Hit http://us.archive.ubuntu.com precise/main i386 Packages
Hit http://us.archive.ubuntu.com precise/restricted i386 Packages
Hit http://security.ubuntu.com precise-security/restricted Sources
Hit http://security.ubuntu.com precise-security/universe Sources
Hit http://security.ubuntu.com precise-security/multiverse Sources
Hit http://security.ubuntu.com precise-security/main amd64 Packages
Hit http://security.ubuntu.com precise-security/restricted amd64 Packages
Hit http://us.archive.ubuntu.com precise/universe i386 Packages
Hit http://us.archive.ubuntu.com precise/multiverse i386 Packages
Hit http://us.archive.ubuntu.com precise/main TranslationIndex
Hit http://us.archive.ubuntu.com precise/multiverse TranslationIndex
Hit http://us.archive.ubuntu.com precise/restricted TranslationIndex
Hit http://us.archive.ubuntu.com precise/universe TranslationIndex
Hit http://us.archive.ubuntu.com precise-updates/main Sources
Hit http://us.archive.ubuntu.com precise-updates/restricted Sources
Hit http://us.archive.ubuntu.com precise-updates/universe Sources
Hit http://us.archive.ubuntu.com precise-updates/multiverse Sources
Hit http://security.ubuntu.com precise-security/universe amd64 Packages
Hit http://security.ubuntu.com precise-security/multiverse amd64 Packages
Hit http://security.ubuntu.com precise-security/main i386 Packages
Hit http://security.ubuntu.com precise-security/restricted i386 Packages
Hit http://security.ubuntu.com precise-security/universe i386 Packages
Hit http://us.archive.ubuntu.com precise-updates/main amd64 Packages
Hit http://us.archive.ubuntu.com precise-updates/restricted amd64 Packages
Hit http://us.archive.ubuntu.com precise-updates/universe amd64 Packages
Hit http://us.archive.ubuntu.com precise-updates/multiverse amd64 Packages
Hit http://us.archive.ubuntu.com precise-updates/main i386 Packages
Hit http://us.archive.ubuntu.com precise-updates/restricted i386 Packages
Hit http://us.archive.ubuntu.com precise-updates/universe i386 Packages
Hit http://us.archive.ubuntu.com precise-updates/multiverse i386 Packages
Hit http://us.archive.ubuntu.com precise-updates/main TranslationIndex
Hit http://us.archive.ubuntu.com precise-updates/multiverse TranslationIndex
Hit http://security.ubuntu.com precise-security/multiverse i386 Packages
Hit http://security.ubuntu.com precise-security/main TranslationIndex
Hit http://security.ubuntu.com precise-security/multiverse TranslationIndex
Hit http://security.ubuntu.com precise-security/restricted TranslationIndex
Hit http://security.ubuntu.com precise-security/universe TranslationIndex
Hit http://us.archive.ubuntu.com precise-updates/restricted TranslationIndex
Hit http://us.archive.ubuntu.com precise-updates/universe TranslationIndex
Hit http://us.archive.ubuntu.com precise-backports/main Sources
Hit http://us.archive.ubuntu.com precise-backports/restricted Sources
Hit http://us.archive.ubuntu.com precise-backports/universe Sources
Hit http://us.archive.ubuntu.com precise-backports/multiverse Sources
Hit http://us.archive.ubuntu.com precise-backports/main amd64 Packages
Hit http://us.archive.ubuntu.com precise-backports/restricted amd64 Packages
Hit http://us.archive.ubuntu.com precise-backports/universe amd64 Packages
Hit http://us.archive.ubuntu.com precise-backports/multiverse amd64 Packages
Hit http://us.archive.ubuntu.com precise-backports/main i386 Packages
Hit http://us.archive.ubuntu.com precise-backports/restricted i386 Packages
Hit http://us.archive.ubuntu.com precise-backports/universe i386 Packages
Hit http://us.archive.ubuntu.com precise-backports/multiverse i386 Packages
Hit http://us.archive.ubuntu.com precise-backports/main TranslationIndex
Hit http://us.archive.ubuntu.com precise-backports/multiverse TranslationIndex
Hit http://us.archive.ubuntu.com precise-backports/restricted TranslationIndex
Hit http://security.ubuntu.com precise-security/main Translation-en
Hit http://security.ubuntu.com precise-security/multiverse Translation-en
Hit http://security.ubuntu.com precise-security/restricted Translation-en
Hit http://us.archive.ubuntu.com precise-backports/universe TranslationIndex
Hit http://us.archive.ubuntu.com precise/main Translation-en
Hit http://us.archive.ubuntu.com precise/multiverse Translation-en
Hit http://us.archive.ubuntu.com precise/restricted Translation-en
Hit http://us.archive.ubuntu.com precise/universe Translation-en
Hit http://us.archive.ubuntu.com precise-updates/main Translation-en
Hit http://us.archive.ubuntu.com precise-updates/multiverse Translation-en
Hit http://us.archive.ubuntu.com precise-updates/restricted Translation-en
Hit http://us.archive.ubuntu.com precise-updates/universe Translation-en
Hit http://us.archive.ubuntu.com precise-backports/main Translation-en
Hit http://security.ubuntu.com precise-security/universe Translation-en
Hit http://us.archive.ubuntu.com precise-backports/multiverse Translation-en
Hit http://us.archive.ubuntu.com precise-backports/restricted Translation-en
Hit http://us.archive.ubuntu.com precise-backports/universe Translation-en
Reading package lists... Done
Reading package lists... Done
Building dependency tree
Reading state information... Done
The following extra packages will be installed:
  git-man libcurl3 liberror-perl
Suggested packages:
  git-daemon-run git-daemon-sysvinit git-doc git-el git-arch git-cvs git-svn git-email git-gui gitk gitweb make-doc
The following NEW packages will be installed:
  curl git git-man libcurl3 liberror-perl software-properties-common
The following packages will be upgraded:
  make
1 upgraded, 6 newly installed, 0 to remove and 136 not upgraded.
Need to get 7,242 kB of archives.
After this operation, 16.3 MB of additional disk space will be used.
Get:1 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main libcurl3 amd64 7.22.0-3ubuntu4.6 [236 kB]
Get:2 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main curl amd64 7.22.0-3ubuntu4.6 [138 kB]
Get:3 http://us.archive.ubuntu.com/ubuntu/ precise/main liberror-perl all 0.17-1 [23.8 kB]
Get:4 http://us.archive.ubuntu.com/ubuntu/ precise/main git-man all 1:1.7.9.5-1 [630 kB]
Get:5 http://us.archive.ubuntu.com/ubuntu/ precise/main git amd64 1:1.7.9.5-1 [6,087 kB]
Get:6 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main make amd64 3.81-8.1ubuntu1.1 [119 kB]
Get:7 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main software-properties-common all 0.82.7.6 [8,846 B]
Fetched 7,242 kB in 7s (975 kB/s)
Selecting previously unselected package libcurl3.
(Reading database ... 60912 files and directories currently installed.)
Unpacking libcurl3 (from .../libcurl3_7.22.0-3ubuntu4.6_amd64.deb) ...
Selecting previously unselected package curl.
Unpacking curl (from .../curl_7.22.0-3ubuntu4.6_amd64.deb) ...
Selecting previously unselected package liberror-perl.
Unpacking liberror-perl (from .../liberror-perl_0.17-1_all.deb) ...
Selecting previously unselected package git-man.
Unpacking git-man (from .../git-man_1%3a1.7.9.5-1_all.deb) ...
Selecting previously unselected package git.
Unpacking git (from .../git_1%3a1.7.9.5-1_amd64.deb) ...
Preparing to replace make 3.81-8.1ubuntu1 (using .../make_3.81-8.1ubuntu1.1_amd64.deb) ...
Unpacking replacement make ...
Selecting previously unselected package software-properties-common.
Unpacking software-properties-common (from .../software-properties-common_0.82.7.6_all.deb) ...
Processing triggers for man-db ...
Setting up libcurl3 (7.22.0-3ubuntu4.6) ...
Setting up curl (7.22.0-3ubuntu4.6) ...
Setting up liberror-perl (0.17-1) ...
Setting up git-man (1:1.7.9.5-1) ...
Setting up git (1:1.7.9.5-1) ...
Setting up make (3.81-8.1ubuntu1.1) ...
Setting up software-properties-common (0.82.7.6) ...
Processing triggers for libc-bin ...
ldconfig deferred processing now taking place
Cloning into 'dokku'...
remote: Reusing existing pack: 1779, done.
remote: Total 1779 (delta 0), reused 0 (delta 0)
Receiving objects: 100% (1779/1779), 332.69 KiB, done.
Resolving deltas: 100% (765/765), done.
Note: checking out 'v0.2.1'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -b with the checkout command again. Example:

  git checkout -b new_branch_name

HEAD is now at b719e63... v0.2.1
wget -qO /usr/local/bin/sshcommand https://raw.github.com/progrium/sshcommand/5f9afe79698332d24a69873721619f5af4670d09/sshcommand
chmod +x /usr/local/bin/sshcommand
sshcommand create dokku /usr/local/bin/dokku
wget -qO /tmp/pluginhook_0.1.0_amd64.deb https://s3.amazonaws.com/progrium-pluginhook/pluginhook_0.1.0_amd64.deb
dpkg -i /tmp/pluginhook_0.1.0_amd64.deb
Selecting previously unselected package pluginhook.
(Reading database ... 61607 files and directories currently installed.)
Unpacking pluginhook (from .../tmp/pluginhook_0.1.0_amd64.deb) ...
Setting up pluginhook (0.1.0) ...
lsmod | grep aufs || modprobe aufs || apt-get install -y linux-image-extra-`uname -r`
egrep -i "^docker" /etc/group || groupadd docker
usermod -aG docker dokku
curl https://get.docker.io/gpg | apt-key add -
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   992  100   992    0     0   2172      0 --:--:-- --:--:-- --:--:--  3397
OK
echo deb http://get.docker.io/ubuntu docker main > /etc/apt/sources.list.d/docker.list
apt-get update
Ign http://get.docker.io docker InRelease
Ign http://us.archive.ubuntu.com precise InRelease
Ign http://us.archive.ubuntu.com precise-updates InRelease
Ign http://us.archive.ubuntu.com precise-backports InRelease
Hit http://us.archive.ubuntu.com precise Release.gpg
Ign http://security.ubuntu.com precise-security InRelease
Hit http://us.archive.ubuntu.com precise-updates Release.gpg
Get:1 http://get.docker.io docker Release.gpg [490 B]
Hit http://us.archive.ubuntu.com precise-backports Release.gpg
Hit http://security.ubuntu.com precise-security Release.gpg
Hit http://us.archive.ubuntu.com precise Release
Get:2 http://get.docker.io docker Release [1,525 B]
Hit http://security.ubuntu.com precise-security Release
Hit http://us.archive.ubuntu.com precise-updates Release
Get:3 http://get.docker.io docker/main amd64 Packages [2,289 B]
Hit http://us.archive.ubuntu.com precise-backports Release
Hit http://us.archive.ubuntu.com precise/main Sources
Hit http://us.archive.ubuntu.com precise/restricted Sources
Hit http://us.archive.ubuntu.com precise/universe Sources
Hit http://us.archive.ubuntu.com precise/multiverse Sources
Hit http://us.archive.ubuntu.com precise/main amd64 Packages
Get:4 http://get.docker.io docker/main i386 Packages [20 B]
Hit http://security.ubuntu.com precise-security/main Sources
Hit http://us.archive.ubuntu.com precise/restricted amd64 Packages
Hit http://us.archive.ubuntu.com precise/universe amd64 Packages
Hit http://us.archive.ubuntu.com precise/multiverse amd64 Packages
Hit http://us.archive.ubuntu.com precise/main i386 Packages
Hit http://us.archive.ubuntu.com precise/restricted i386 Packages
Hit http://us.archive.ubuntu.com precise/universe i386 Packages
Hit http://us.archive.ubuntu.com precise/multiverse i386 Packages
Hit http://us.archive.ubuntu.com precise/main TranslationIndex
Hit http://us.archive.ubuntu.com precise/multiverse TranslationIndex
Hit http://us.archive.ubuntu.com precise/restricted TranslationIndex
Hit http://us.archive.ubuntu.com precise/universe TranslationIndex
Hit http://us.archive.ubuntu.com precise-updates/main Sources
Hit http://us.archive.ubuntu.com precise-updates/restricted Sources
Hit http://us.archive.ubuntu.com precise-updates/universe Sources
Ign http://get.docker.io docker/main TranslationIndex
Hit http://security.ubuntu.com precise-security/restricted Sources
Hit http://security.ubuntu.com precise-security/universe Sources
Hit http://security.ubuntu.com precise-security/multiverse Sources
Hit http://security.ubuntu.com precise-security/main amd64 Packages
Hit http://security.ubuntu.com precise-security/restricted amd64 Packages
Hit http://us.archive.ubuntu.com precise-updates/multiverse Sources
Hit http://us.archive.ubuntu.com precise-updates/main amd64 Packages
Hit http://us.archive.ubuntu.com precise-updates/restricted amd64 Packages
Hit http://us.archive.ubuntu.com precise-updates/universe amd64 Packages
Hit http://us.archive.ubuntu.com precise-updates/multiverse amd64 Packages
Hit http://us.archive.ubuntu.com precise-updates/main i386 Packages
Hit http://us.archive.ubuntu.com precise-updates/restricted i386 Packages
Hit http://us.archive.ubuntu.com precise-updates/universe i386 Packages
Hit http://us.archive.ubuntu.com precise-updates/multiverse i386 Packages
Hit http://us.archive.ubuntu.com precise-updates/main TranslationIndex
Hit http://us.archive.ubuntu.com precise-updates/multiverse TranslationIndex
Hit http://security.ubuntu.com precise-security/universe amd64 Packages
Hit http://security.ubuntu.com precise-security/multiverse amd64 Packages
Hit http://security.ubuntu.com precise-security/main i386 Packages
Hit http://security.ubuntu.com precise-security/restricted i386 Packages
Hit http://security.ubuntu.com precise-security/universe i386 Packages
Hit http://us.archive.ubuntu.com precise-updates/restricted TranslationIndex
Hit http://us.archive.ubuntu.com precise-updates/universe TranslationIndex
Hit http://us.archive.ubuntu.com precise-backports/main Sources
Hit http://us.archive.ubuntu.com precise-backports/restricted Sources
Hit http://us.archive.ubuntu.com precise-backports/universe Sources
Hit http://security.ubuntu.com precise-security/multiverse i386 Packages
Hit http://security.ubuntu.com precise-security/main TranslationIndex
Hit http://security.ubuntu.com precise-security/multiverse TranslationIndex
Hit http://security.ubuntu.com precise-security/restricted TranslationIndex
Hit http://security.ubuntu.com precise-security/universe TranslationIndex
Hit http://us.archive.ubuntu.com precise-backports/multiverse Sources
Hit http://us.archive.ubuntu.com precise-backports/main amd64 Packages
Hit http://us.archive.ubuntu.com precise-backports/restricted amd64 Packages
Hit http://us.archive.ubuntu.com precise-backports/universe amd64 Packages
Hit http://us.archive.ubuntu.com precise-backports/multiverse amd64 Packages
Hit http://us.archive.ubuntu.com precise-backports/main i386 Packages
Hit http://us.archive.ubuntu.com precise-backports/restricted i386 Packages
Hit http://security.ubuntu.com precise-security/main Translation-en
Hit http://security.ubuntu.com precise-security/multiverse Translation-en
Hit http://security.ubuntu.com precise-security/restricted Translation-en
Hit http://security.ubuntu.com precise-security/universe Translation-en
Hit http://us.archive.ubuntu.com precise-backports/universe i386 Packages
Hit http://us.archive.ubuntu.com precise-backports/multiverse i386 Packages
Hit http://us.archive.ubuntu.com precise-backports/main TranslationIndex
Hit http://us.archive.ubuntu.com precise-backports/multiverse TranslationIndex
Hit http://us.archive.ubuntu.com precise-backports/restricted TranslationIndex
Hit http://us.archive.ubuntu.com precise-backports/universe TranslationIndex
Hit http://us.archive.ubuntu.com precise/main Translation-en
Hit http://us.archive.ubuntu.com precise/multiverse Translation-en
Hit http://us.archive.ubuntu.com precise/restricted Translation-en
Hit http://us.archive.ubuntu.com precise/universe Translation-en
Hit http://us.archive.ubuntu.com precise-updates/main Translation-en
Hit http://us.archive.ubuntu.com precise-updates/multiverse Translation-en
Hit http://us.archive.ubuntu.com precise-updates/restricted Translation-en
Hit http://us.archive.ubuntu.com precise-updates/universe Translation-en
Hit http://us.archive.ubuntu.com precise-backports/main Translation-en
Hit http://us.archive.ubuntu.com precise-backports/multiverse Translation-en
Hit http://us.archive.ubuntu.com precise-backports/restricted Translation-en
Hit http://us.archive.ubuntu.com precise-backports/universe Translation-en
Ign http://get.docker.io docker/main Translation-en_US
Ign http://get.docker.io docker/main Translation-en
Fetched 4,324 B in 2s (1,533 B/s)
Reading package lists... Done
apt-get install -y lxc-docker
Reading package lists... Done
Building dependency tree
Reading state information... Done
The following extra packages will be installed:
  aufs-tools bridge-utils cgroup-lite cloud-utils debootstrap dnsmasq-base euca2ools libapparmor1 libcap2 libcap2-bin
  libnetfilter-conntrack3 libpam-cap libyaml-0-2 lxc lxc-docker-0.7.3 python-boto python-crypto python-m2crypto
  python-paramiko python-yaml
Suggested packages:
  libcap-dev btrfs-tools qemu-user-static python-crypto-dbg python-crypto-doc
The following NEW packages will be installed:
  aufs-tools bridge-utils cgroup-lite cloud-utils debootstrap dnsmasq-base euca2ools libapparmor1 libcap2 libcap2-bin
  libnetfilter-conntrack3 libpam-cap libyaml-0-2 lxc lxc-docker lxc-docker-0.7.3 python-boto python-crypto
  python-m2crypto python-paramiko python-yaml
0 upgraded, 21 newly installed, 0 to remove and 136 not upgraded.
Need to get 5,424 kB of archives.
After this operation, 30.4 MB of additional disk space will be used.
Get:1 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main bridge-utils amd64 1.5-2ubuntu7 [32.0 kB]
Get:2 http://get.docker.io/ubuntu/ docker/main lxc-docker-0.7.3 amd64 0.7.3 [2,677 kB]
Get:3 http://us.archive.ubuntu.com/ubuntu/ precise/main libcap2 amd64 1:2.22-1ubuntu3 [12.0 kB]
Get:4 http://us.archive.ubuntu.com/ubuntu/ precise/main libyaml-0-2 amd64 0.1.4-2 [56.9 kB]
Get:5 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main libapparmor1 amd64 2.7.102-0ubuntu3.9 [37.6 kB]
Get:6 http://us.archive.ubuntu.com/ubuntu/ precise/main libnetfilter-conntrack3 amd64 0.9.1-1ubuntu1 [34.4 kB]
Get:7 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main dnsmasq-base amd64 2.59-4ubuntu0.1 [213 kB]
Get:8 http://us.archive.ubuntu.com/ubuntu/ precise-updates/universe lxc amd64 0.7.5-3ubuntu69 [173 kB]
Get:9 http://us.archive.ubuntu.com/ubuntu/ precise/main python-m2crypto amd64 0.21.1-2ubuntu2 [157 kB]
Get:10 http://us.archive.ubuntu.com/ubuntu/ precise/universe aufs-tools amd64 1:3.0+20111101-1ubuntu1 [98.8 kB]
Get:11 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main python-boto all 2.2.2-0ubuntu3 [441 kB]
Get:12 http://get.docker.io/ubuntu/ docker/main lxc-docker amd64 0.7.3 [1,870 B]
Get:13 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main euca2ools all 2.0.0~bzr516-0ubuntu3.1 [179 kB]
Get:14 http://us.archive.ubuntu.com/ubuntu/ precise/main libcap2-bin amd64 1:2.22-1ubuntu3 [17.6 kB]
Get:15 http://us.archive.ubuntu.com/ubuntu/ precise/main libpam-cap amd64 1:2.22-1ubuntu3 [7,704 B]
Get:16 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main python-crypto amd64 2.4.1-1ubuntu0.1 [293 kB]
Get:17 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main python-paramiko all 1.7.7.1-2ubuntu1 [797 kB]
Get:18 http://us.archive.ubuntu.com/ubuntu/ precise/main python-yaml amd64 3.10-2 [122 kB]
Get:19 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main cgroup-lite all 1.1.2 [3,878 B]
Get:20 http://us.archive.ubuntu.com/ubuntu/ precise/main cloud-utils all 0.25-0ubuntu5 [35.1 kB]
Get:21 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main debootstrap all 1.0.40~ubuntu0.4 [34.3 kB]
Fetched 5,424 kB in 8s (639 kB/s)
Selecting previously unselected package bridge-utils.
(Reading database ... 61610 files and directories currently installed.)
Unpacking bridge-utils (from .../bridge-utils_1.5-2ubuntu7_amd64.deb) ...
Selecting previously unselected package libcap2.
Unpacking libcap2 (from .../libcap2_1%3a2.22-1ubuntu3_amd64.deb) ...
Selecting previously unselected package libyaml-0-2.
Unpacking libyaml-0-2 (from .../libyaml-0-2_0.1.4-2_amd64.deb) ...
Selecting previously unselected package libapparmor1.
Unpacking libapparmor1 (from .../libapparmor1_2.7.102-0ubuntu3.9_amd64.deb) ...
Selecting previously unselected package libnetfilter-conntrack3.
Unpacking libnetfilter-conntrack3 (from .../libnetfilter-conntrack3_0.9.1-1ubuntu1_amd64.deb) ...
Selecting previously unselected package dnsmasq-base.
Unpacking dnsmasq-base (from .../dnsmasq-base_2.59-4ubuntu0.1_amd64.deb) ...
Selecting previously unselected package lxc.
Unpacking lxc (from .../lxc_0.7.5-3ubuntu69_amd64.deb) ...
Selecting previously unselected package python-m2crypto.
Unpacking python-m2crypto (from .../python-m2crypto_0.21.1-2ubuntu2_amd64.deb) ...
Selecting previously unselected package aufs-tools.
Unpacking aufs-tools (from .../aufs-tools_1%3a3.0+20111101-1ubuntu1_amd64.deb) ...
Selecting previously unselected package python-boto.
Unpacking python-boto (from .../python-boto_2.2.2-0ubuntu3_all.deb) ...
Selecting previously unselected package euca2ools.
Unpacking euca2ools (from .../euca2ools_2.0.0~bzr516-0ubuntu3.1_all.deb) ...
Selecting previously unselected package libcap2-bin.
Unpacking libcap2-bin (from .../libcap2-bin_1%3a2.22-1ubuntu3_amd64.deb) ...
Selecting previously unselected package libpam-cap.
Unpacking libpam-cap (from .../libpam-cap_1%3a2.22-1ubuntu3_amd64.deb) ...
Selecting previously unselected package python-crypto.
Unpacking python-crypto (from .../python-crypto_2.4.1-1ubuntu0.1_amd64.deb) ...
Selecting previously unselected package python-paramiko.
Unpacking python-paramiko (from .../python-paramiko_1.7.7.1-2ubuntu1_all.deb) ...
Selecting previously unselected package python-yaml.
Unpacking python-yaml (from .../python-yaml_3.10-2_amd64.deb) ...
Selecting previously unselected package cgroup-lite.
Unpacking cgroup-lite (from .../cgroup-lite_1.1.2_all.deb) ...
Selecting previously unselected package cloud-utils.
Unpacking cloud-utils (from .../cloud-utils_0.25-0ubuntu5_all.deb) ...
Selecting previously unselected package debootstrap.
Unpacking debootstrap (from .../debootstrap_1.0.40~ubuntu0.4_all.deb) ...
Selecting previously unselected package lxc-docker-0.7.3.
Unpacking lxc-docker-0.7.3 (from .../lxc-docker-0.7.3_0.7.3_amd64.deb) ...
Selecting previously unselected package lxc-docker.
Unpacking lxc-docker (from .../lxc-docker_0.7.3_amd64.deb) ...
Processing triggers for man-db ...
Processing triggers for ureadahead ...
ureadahead will be reprofiled on next reboot
Setting up bridge-utils (1.5-2ubuntu7) ...
Setting up libcap2 (1:2.22-1ubuntu3) ...
Setting up libyaml-0-2 (0.1.4-2) ...
Setting up libapparmor1 (2.7.102-0ubuntu3.9) ...
Setting up libnetfilter-conntrack3 (0.9.1-1ubuntu1) ...
Setting up dnsmasq-base (2.59-4ubuntu0.1) ...
Setting up lxc (0.7.5-3ubuntu69) ...
lxc start/running
Setting up lxc dnsmasq configuration.
Setting up python-m2crypto (0.21.1-2ubuntu2) ...
Setting up aufs-tools (1:3.0+20111101-1ubuntu1) ...
Setting up python-boto (2.2.2-0ubuntu3) ...
Setting up euca2ools (2.0.0~bzr516-0ubuntu3.1) ...
Setting up libcap2-bin (1:2.22-1ubuntu3) ...
Setting up libpam-cap (1:2.22-1ubuntu3) ...
Setting up python-crypto (2.4.1-1ubuntu0.1) ...
Setting up python-paramiko (1.7.7.1-2ubuntu1) ...
Setting up python-yaml (3.10-2) ...
Setting up cgroup-lite (1.1.2) ...
cgroup-lite start/running
Setting up cloud-utils (0.25-0ubuntu5) ...
Setting up debootstrap (1.0.40~ubuntu0.4) ...
Setting up lxc-docker-0.7.3 (0.7.3) ...
docker start/running, process 6408
Setting up lxc-docker (0.7.3) ...
Processing triggers for libc-bin ...
ldconfig deferred processing now taking place
sleep 2 # give docker a moment i guess
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  309M  100  309M    0     0   968k      0  0:05:27  0:05:27 --:--:-- 1124k
98c2cdf598132b7672b1729d2e1ce4f4505302edaf18b41bcedc3297c79e65ff
cp dokku /usr/local/bin/dokku
mkdir -p /var/lib/dokku/plugins
cp -r plugins/* /var/lib/dokku/plugins
dokku plugins-install
gpg: keyring `/tmp/tmp62bNqo/secring.gpg' created
gpg: keyring `/tmp/tmp62bNqo/pubring.gpg' created
gpg: requesting key C300EE8C from hkp server keyserver.ubuntu.com
gpg: /tmp/tmp62bNqo/trustdb.gpg: trustdb created
gpg: key C300EE8C: public key "Launchpad Stable" imported
gpg: no ultimately trusted keys found
gpg: Total number processed: 1
gpg:               imported: 1  (RSA: 1)
OK
Ign http://us.archive.ubuntu.com precise InRelease
Ign http://us.archive.ubuntu.com precise-updates InRelease
Ign http://us.archive.ubuntu.com precise-backports InRelease
Ign http://get.docker.io docker InRelease
Ign http://ppa.launchpad.net precise InRelease
Hit http://us.archive.ubuntu.com precise Release.gpg
Hit http://us.archive.ubuntu.com precise-updates Release.gpg
Ign http://security.ubuntu.com precise-security InRelease
Hit http://us.archive.ubuntu.com precise-backports Release.gpg
Get:1 http://ppa.launchpad.net precise Release.gpg [316 B]
Hit http://us.archive.ubuntu.com precise Release
Hit http://get.docker.io docker Release.gpg
Hit http://security.ubuntu.com precise-security Release.gpg
Hit http://us.archive.ubuntu.com precise-updates Release
Get:2 http://ppa.launchpad.net precise Release [11.9 kB]
Hit http://us.archive.ubuntu.com precise-backports Release
Hit http://us.archive.ubuntu.com precise/main Sources
Hit http://us.archive.ubuntu.com precise/restricted Sources
Hit http://us.archive.ubuntu.com precise/universe Sources
Hit http://us.archive.ubuntu.com precise/multiverse Sources
Hit http://us.archive.ubuntu.com precise/main amd64 Packages
Hit http://get.docker.io docker Release
Hit http://security.ubuntu.com precise-security Release
Hit http://us.archive.ubuntu.com precise/restricted amd64 Packages
Hit http://us.archive.ubuntu.com precise/universe amd64 Packages
Hit http://us.archive.ubuntu.com precise/multiverse amd64 Packages
Hit http://us.archive.ubuntu.com precise/main i386 Packages
Hit http://us.archive.ubuntu.com precise/restricted i386 Packages
Hit http://us.archive.ubuntu.com precise/universe i386 Packages
Hit http://us.archive.ubuntu.com precise/multiverse i386 Packages
Hit http://us.archive.ubuntu.com precise/main TranslationIndex
Hit http://us.archive.ubuntu.com precise/multiverse TranslationIndex
Hit http://us.archive.ubuntu.com precise/restricted TranslationIndex
Hit http://us.archive.ubuntu.com precise/universe TranslationIndex
Hit http://us.archive.ubuntu.com precise-updates/main Sources
Hit http://us.archive.ubuntu.com precise-updates/restricted Sources
Hit http://us.archive.ubuntu.com precise-updates/universe Sources
Hit http://us.archive.ubuntu.com precise-updates/multiverse Sources
Hit http://security.ubuntu.com precise-security/main Sources
Hit http://us.archive.ubuntu.com precise-updates/main amd64 Packages
Hit http://us.archive.ubuntu.com precise-updates/restricted amd64 Packages
Hit http://get.docker.io docker/main amd64 Packages
Get:3 http://ppa.launchpad.net precise/main Sources [1,566 B]
Hit http://us.archive.ubuntu.com precise-updates/universe amd64 Packages
Hit http://us.archive.ubuntu.com precise-updates/multiverse amd64 Packages
Hit http://us.archive.ubuntu.com precise-updates/main i386 Packages
Hit http://us.archive.ubuntu.com precise-updates/restricted i386 Packages
Hit http://us.archive.ubuntu.com precise-updates/universe i386 Packages
Hit http://us.archive.ubuntu.com precise-updates/multiverse i386 Packages
Hit http://us.archive.ubuntu.com precise-updates/main TranslationIndex
Hit http://us.archive.ubuntu.com precise-updates/multiverse TranslationIndex
Hit http://us.archive.ubuntu.com precise-updates/restricted TranslationIndex
Hit http://us.archive.ubuntu.com precise-updates/universe TranslationIndex
Hit http://us.archive.ubuntu.com precise-backports/main Sources
Hit http://us.archive.ubuntu.com precise-backports/restricted Sources
Hit http://us.archive.ubuntu.com precise-backports/universe Sources
Hit http://get.docker.io docker/main i386 Packages
Hit http://security.ubuntu.com precise-security/restricted Sources
Hit http://security.ubuntu.com precise-security/universe Sources
Hit http://security.ubuntu.com precise-security/multiverse Sources
Hit http://security.ubuntu.com precise-security/main amd64 Packages
Hit http://security.ubuntu.com precise-security/restricted amd64 Packages
Get:4 http://ppa.launchpad.net precise/main amd64 Packages [5,575 B]
Get:5 http://ppa.launchpad.net precise/main i386 Packages [5,575 B]
Hit http://us.archive.ubuntu.com precise-backports/multiverse Sources
Hit http://us.archive.ubuntu.com precise-backports/main amd64 Packages
Hit http://us.archive.ubuntu.com precise-backports/restricted amd64 Packages
Hit http://us.archive.ubuntu.com precise-backports/universe amd64 Packages
Hit http://us.archive.ubuntu.com precise-backports/multiverse amd64 Packages
Hit http://us.archive.ubuntu.com precise-backports/main i386 Packages
Hit http://us.archive.ubuntu.com precise-backports/restricted i386 Packages
Hit http://us.archive.ubuntu.com precise-backports/universe i386 Packages
Hit http://us.archive.ubuntu.com precise-backports/multiverse i386 Packages
Hit http://us.archive.ubuntu.com precise-backports/main TranslationIndex
Hit http://us.archive.ubuntu.com precise-backports/multiverse TranslationIndex
Hit http://us.archive.ubuntu.com precise-backports/restricted TranslationIndex
Hit http://us.archive.ubuntu.com precise-backports/universe TranslationIndex
Hit http://us.archive.ubuntu.com precise/main Translation-en
Hit http://us.archive.ubuntu.com precise/multiverse Translation-en
Hit http://us.archive.ubuntu.com precise/restricted Translation-en
Hit http://us.archive.ubuntu.com precise/universe Translation-en
Ign http://ppa.launchpad.net precise/main TranslationIndex
Hit http://security.ubuntu.com precise-security/universe amd64 Packages
Hit http://security.ubuntu.com precise-security/multiverse amd64 Packages
Hit http://security.ubuntu.com precise-security/main i386 Packages
Hit http://security.ubuntu.com precise-security/restricted i386 Packages
Hit http://security.ubuntu.com precise-security/universe i386 Packages
Ign http://get.docker.io docker/main TranslationIndex
Hit http://us.archive.ubuntu.com precise-updates/main Translation-en
Hit http://us.archive.ubuntu.com precise-updates/multiverse Translation-en
Hit http://us.archive.ubuntu.com precise-updates/restricted Translation-en
Hit http://us.archive.ubuntu.com precise-updates/universe Translation-en
Hit http://us.archive.ubuntu.com precise-backports/main Translation-en
Hit http://us.archive.ubuntu.com precise-backports/multiverse Translation-en
Hit http://us.archive.ubuntu.com precise-backports/restricted Translation-en
Hit http://us.archive.ubuntu.com precise-backports/universe Translation-en
Hit http://security.ubuntu.com precise-security/multiverse i386 Packages
Hit http://security.ubuntu.com precise-security/main TranslationIndex
Hit http://security.ubuntu.com precise-security/multiverse TranslationIndex
Hit http://security.ubuntu.com precise-security/restricted TranslationIndex
Hit http://security.ubuntu.com precise-security/universe TranslationIndex
Hit http://security.ubuntu.com precise-security/main Translation-en
Hit http://security.ubuntu.com precise-security/multiverse Translation-en
Hit http://security.ubuntu.com precise-security/restricted Translation-en
Hit http://security.ubuntu.com precise-security/universe Translation-en
Ign http://ppa.launchpad.net precise/main Translation-en_US
Ign http://ppa.launchpad.net precise/main Translation-en
Ign http://get.docker.io docker/main Translation-en_US
Ign http://get.docker.io docker/main Translation-en
Fetched 24.9 kB in 2s (11.3 kB/s)
Reading package lists... Done
Reading package lists... Done
Building dependency tree
Reading state information... Done
The following extra packages will be installed:
  bind9-host init-system-helpers libbind9-80 libdns81 libgd2-noxpm libisc83 libisccfg82 libjpeg-turbo8 libjpeg8
  liblwres80 libxslt1.1 nginx-common nginx-full
Suggested packages:
  rblcheck libgd-tools fcgiwrap nginx-doc
The following NEW packages will be installed:
  init-system-helpers libgd2-noxpm libjpeg-turbo8 libjpeg8 libxslt1.1 nginx nginx-common nginx-full
The following packages will be upgraded:
  bind9-host dnsutils libbind9-80 libdns81 libisc83 libisccfg82 liblwres80
7 upgraded, 8 newly installed, 0 to remove and 129 not upgraded.
Need to get 2,273 kB of archives.
After this operation, 2,844 kB of additional disk space will be used.
Get:1 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main libjpeg-turbo8 amd64 1.1.90+svn733-0ubuntu4.3 [111 kB]
Get:2 http://ppa.launchpad.net/nginx/stable/ubuntu/ precise/main init-system-helpers all 1.7~precise1~ppa1 [10.6 kB]
Get:3 http://ppa.launchpad.net/nginx/stable/ubuntu/ precise/main nginx-common all 1.4.4-1~precise0 [78.0 kB]
Get:4 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main libxslt1.1 amd64 1.1.26-8ubuntu1.3 [167 kB]
Get:5 http://us.archive.ubuntu.com/ubuntu/ precise/main libjpeg8 amd64 8c-2ubuntu7 [2,112 B]
Get:6 http://us.archive.ubuntu.com/ubuntu/ precise/main libgd2-noxpm amd64 2.0.36~rc1~dfsg-6ubuntu2 [200 kB]
Get:7 http://ppa.launchpad.net/nginx/stable/ubuntu/ precise/main nginx-full amd64 1.4.4-1~precise0 [464 kB]
Get:8 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main bind9-host amd64 1:9.8.1.dfsg.P1-4ubuntu0.7 [55.3 kB]
Get:9 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main dnsutils amd64 1:9.8.1.dfsg.P1-4ubuntu0.7 [148 kB]
Get:10 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main libisc83 amd64 1:9.8.1.dfsg.P1-4ubuntu0.7 [161 kB]
Get:11 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main libdns81 amd64 1:9.8.1.dfsg.P1-4ubuntu0.7 [704 kB]
Get:12 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main libisccfg82 amd64 1:9.8.1.dfsg.P1-4ubuntu0.7 [43.4 kB]
Get:13 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main liblwres80 amd64 1:9.8.1.dfsg.P1-4ubuntu0.7 [37.9 kB]
Get:14 http://us.archive.ubuntu.com/ubuntu/ precise-updates/main libbind9-80 amd64 1:9.8.1.dfsg.P1-4ubuntu0.7 [24.3 kB]
Get:15 http://ppa.launchpad.net/nginx/stable/ubuntu/ precise/main nginx all 1.4.4-1~precise0 [66.7 kB]
Fetched 2,273 kB in 6s (338 kB/s)
Selecting previously unselected package libjpeg-turbo8.
(Reading database ... 63855 files and directories currently installed.)
Unpacking libjpeg-turbo8 (from .../libjpeg-turbo8_1.1.90+svn733-0ubuntu4.3_amd64.deb) ...
Selecting previously unselected package libxslt1.1.
Unpacking libxslt1.1 (from .../libxslt1.1_1.1.26-8ubuntu1.3_amd64.deb) ...
Selecting previously unselected package libjpeg8.
Unpacking libjpeg8 (from .../libjpeg8_8c-2ubuntu7_amd64.deb) ...
Selecting previously unselected package libgd2-noxpm.
Unpacking libgd2-noxpm (from .../libgd2-noxpm_2.0.36~rc1~dfsg-6ubuntu2_amd64.deb) ...
Preparing to replace bind9-host 1:9.8.1.dfsg.P1-4ubuntu0.3 (using .../bind9-host_1%3a9.8.1.dfsg.P1-4ubuntu0.7_amd64.deb) ...
Unpacking replacement bind9-host ...
Preparing to replace dnsutils 1:9.8.1.dfsg.P1-4ubuntu0.3 (using .../dnsutils_1%3a9.8.1.dfsg.P1-4ubuntu0.7_amd64.deb) ...
Unpacking replacement dnsutils ...
Preparing to replace libisc83 1:9.8.1.dfsg.P1-4ubuntu0.3 (using .../libisc83_1%3a9.8.1.dfsg.P1-4ubuntu0.7_amd64.deb) ...
Unpacking replacement libisc83 ...
Preparing to replace libdns81 1:9.8.1.dfsg.P1-4ubuntu0.3 (using .../libdns81_1%3a9.8.1.dfsg.P1-4ubuntu0.7_amd64.deb) ...
Unpacking replacement libdns81 ...
Preparing to replace libisccfg82 1:9.8.1.dfsg.P1-4ubuntu0.3 (using .../libisccfg82_1%3a9.8.1.dfsg.P1-4ubuntu0.7_amd64.deb) ...
Unpacking replacement libisccfg82 ...
Preparing to replace liblwres80 1:9.8.1.dfsg.P1-4ubuntu0.3 (using .../liblwres80_1%3a9.8.1.dfsg.P1-4ubuntu0.7_amd64.deb) ...
Unpacking replacement liblwres80 ...
Preparing to replace libbind9-80 1:9.8.1.dfsg.P1-4ubuntu0.3 (using .../libbind9-80_1%3a9.8.1.dfsg.P1-4ubuntu0.7_amd64.deb) ...
Unpacking replacement libbind9-80 ...
Selecting previously unselected package init-system-helpers.
Unpacking init-system-helpers (from .../init-system-helpers_1.7~precise1~ppa1_all.deb) ...
Selecting previously unselected package nginx-common.
Unpacking nginx-common (from .../nginx-common_1.4.4-1~precise0_all.deb) ...
Selecting previously unselected package nginx-full.
Unpacking nginx-full (from .../nginx-full_1.4.4-1~precise0_amd64.deb) ...
Selecting previously unselected package nginx.
Unpacking nginx (from .../nginx_1.4.4-1~precise0_all.deb) ...
Processing triggers for man-db ...
Processing triggers for ufw ...
Processing triggers for ureadahead ...
Setting up libjpeg-turbo8 (1.1.90+svn733-0ubuntu4.3) ...
Setting up libxslt1.1 (1.1.26-8ubuntu1.3) ...
Setting up libjpeg8 (8c-2ubuntu7) ...
Setting up libgd2-noxpm (2.0.36~rc1~dfsg-6ubuntu2) ...
Setting up libisc83 (1:9.8.1.dfsg.P1-4ubuntu0.7) ...
Setting up libdns81 (1:9.8.1.dfsg.P1-4ubuntu0.7) ...
Setting up libisccfg82 (1:9.8.1.dfsg.P1-4ubuntu0.7) ...
Setting up libbind9-80 (1:9.8.1.dfsg.P1-4ubuntu0.7) ...
Setting up liblwres80 (1:9.8.1.dfsg.P1-4ubuntu0.7) ...
Setting up bind9-host (1:9.8.1.dfsg.P1-4ubuntu0.7) ...
Setting up dnsutils (1:9.8.1.dfsg.P1-4ubuntu0.7) ...
Setting up init-system-helpers (1.7~precise1~ppa1) ...
Setting up nginx-common (1.4.4-1~precise0) ...
ln -s '/lib/systemd/system/nginx.service' '/etc/systemd/system/multi-user.target.wants/nginx.service'
Setting up nginx-full (1.4.4-1~precise0) ...
Setting up nginx (1.4.4-1~precise0) ...
Processing triggers for libc-bin ...
ldconfig deferred processing now taking place
 * Starting nginx nginx                                                                                          [ OK ]
git describe --tags > /home/dokku/VERSION  2> /dev/null || echo '~v0.2.1 (2014-01-05T21:34+0000)' > /home/dokku/VERSION

Almost done! For next steps on configuration:
  https://github.com/progrium/dokku#configuring
```
