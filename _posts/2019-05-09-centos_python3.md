---
title: "Python 3.7.3 on CentOS 7"
excerpt: Setting up the latest version of Python on CentOS 7.
categories: tech
thumbnail: wrench
series: CentOS
published: true
---
!["Python"](/images/python-logo-for-blog.png)

It's always a pain to install Python 3 on CentOS because they don't allow the cutting edge Python packages in their repositories (and even epel is a few versions behind). We need to run the following commands to build and install Python 3.7.3 (the latest version at the time of this writing):

```
$ sudo -i
$ yum groupinstall -y "development tools"
$ yum install -y \
  libffi-devel \
  zlib-devel \
  bzip2-devel \
  openssl-devel \
  ncurses-devel \
  sqlite-devel \
  readline-devel \
  tk-devel \
  gdbm-devel \
  db4-devel \
  libpcap-devel \
  xz-devel \
  expat-devel

$ cd /usr/src
$ wget http://python.org/ftp/python/3.7.3/Python-3.7.3.tar.xz
$ tar xf Python-3.7.3.tar.xz
$ cd Python-3.7.3
$ ./configure --enable-optimizations
$ make altinstall
$ exit
```

Use the command ``` make altinstall ``` so that we don't replace the built in Python (2.7.5) executable which is used for system-wide processes.

Whilst you are still root, check to make sure that __secure_path__ in __/etc/sudoers__ file includes /usr/local/bin. The line should look like this:

```
Defaults    secure_path = /sbin:/bin:/usr/sbin:/usr/bin:/usr/local/bin
```

Also while you're in there, now is a good time to check our version of pip.

```
$ sudo pip3.7 install --upgrade pip
```

Finally, because typing ```$ python3.7``` every time we turn around would be a drag, we can change the prompt to ```$ python3``` by adding an alias to the __.bashrc__ file: 

```
# User specific aliases and functions
alias python3=python3.7
```

!["CentOS 7"](/images/CentOS.png)
