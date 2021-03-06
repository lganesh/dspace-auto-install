dspace-auto-install
===================

Automatic install DSpace on Ubuntu like systems.

This project was based in article LiveCD on [Wiki DSpace](https://wiki.duraspace.org/display/DSPACE/LiveCD).

http://royopa.wordpress.com/2014/03/04/instalacao-do-dspace-4-1-em-sistemas-ubuntu-like/

Download a Linux Image
----------------------

To avoid the install process, we download a imagem with Ubuntu Server Linux.

Ubuntu Linux Server Edition 14.04 x86

Size (compressed/uncompressed): 430 MB/1.4 GB

MD5SUM of ova image: 7afed719e42e59f870509b6ffe53c442

Link: https://s3-eu-west-1.amazonaws.com/virtualboxes.org/ubuntu-14.04-server-i386.ova.torrent

Active user account(s)(username/password): **ubuntu/reverse**

Getting Started
---------------

```shell
cd ~
wget https://github.com/royopa/dspace-auto-install/archive/master.zip
unzip master.zip
cd dspace-auto-install-master
```

Change the parameters
---------------------

Change the parameters in according to your needs:

build-dspace
------------

    VERSION_DSPACE="5.2"
    
build.properties
----------------

    dspace.name = DSpace
    default.language = pt_BR
    
dspace.cfg
----------

    dspace.name = DSpace
    default.language = pt_BR
    mail.server=smtp.gmail.com
    mail.server.username = treinamento.dspace@gmail.com
    mail.server.password = yourPassword
    mail.extraproperties = mail.smtp.socketFactory.port=465, \
    mail.smtp.socketFactory.class=javax.net.ssl.SSLSocketFactory, \
    mail.smtp.socketFactory.fallback=false
    mail.from.address = treinamento.dspace@gmail.com
    feedback.recipient = treinamento.dspace@gmail.com
    mail.admin = treinamento.dspace@gmail.com
    alert.recipient = treinamento.dspace@gmail.com
    registration.notify = treinamento.dspace@gmail.com
    
Install
-------
Execute the install script

```shell
./build-dspace
```

So, access the application with links below:

[http://localhost:8080/xmlui/](http://localhost:8080/xmlui/)

[http://localhost:8080/jspui/](http://localhost:8080/jspui/)

[http://localhost:8080/oai/](http://localhost:8080/oai/)


Vagrant
-------

You can use vagrant to test the install. For this, follow the commands below:

Install plugins:

```sh
vagrant plugin install landrush
vagrant plugin install vagrant-vbguest
vagrant plugin install vagrant-cachier
```

And start the virtual machine

```sh
vagrant up
```

So, access the application with links below:

[http://localhost:8080/xmlui/](http://localhost:8080/xmlui/)

[http://localhost:8080/jspui/](http://localhost:8080/jspui/)

[http://localhost:8080/oai/](http://localhost:8080/oai/)

Extra
-----

See below how to script works:

[![asciicast](https://asciinema.org/a/10778.png)](https://asciinema.org/a/10778)
