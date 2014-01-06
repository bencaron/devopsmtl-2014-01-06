# post-install setup

See [Dokku configuration instructions.](https://github.com/progrium/dokku#configuring)

## setup the hostname

If your host has a properly setup domain name, the installation process will do this automatically. But if not (for exemple on a Vagrant box), you will have to do it manually:

```
root@vagrant:~# cd /home/dokku/
root@vagrant:/home/dokku# ls
HOSTNAME  VERSION
root@vagrant:/home/dokku# cat HOSTNAME
vagrant.vm
root@vagrant:/home/dokku# vim VHOST
root@vagrant:/home/dokku# cat VHOST
exemple.com
```

## Add a public key


```bash
root@vagrant:/vagrant# cat /vagrant/id_rsa.pub | sshcommand acl-add dokku myapp
```

Or do it remotely:

```bash
$ cat ~/.ssh/id_rsa.pub | ssh exemple.com "sudo sshcommand acl-add dokku myapp"
```