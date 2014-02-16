# Description
This configuration includes following software:

* PHP 5.4.19 
* MySQL 5.5.32
* GIT 1.7.9.5
* Apache 2.2.22
* Vim
* MC (Midnight commander)
* Curl
* Composer

# Usage

First you need to create vagrant VM

```
$ cd vagrant
$ vagrant up
```

While waiting for Vagrant to start up, you should add an entry into /etc/hosts file on the host machine.

```
10.0.0.200      volleyball.dev
```

From now you should be able to access your Volleyball project at [http://volleyball.dev/](http://volleyball.dev/)

# Troubleshooting

Using Symfony2 inside Vagrant can be slow due to synchronisation delay incurred by NFS. To avoid this, both locations have been have been moved to a shared memory segment under ``/dev/shm/volleyball``.

To view the application logs, run the following commands:

```bash
$ tail -f /dev/shm/volleyball/app/logs/prod.log
$ tail -f /dev/shm/volleyball/app/logs/dev.log
```