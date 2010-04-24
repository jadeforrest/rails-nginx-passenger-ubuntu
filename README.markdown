rails-nginx-passenger-ubuntu
============================

Adopted notes on setting up a simple production server with ubuntu,
nginx, passenger, mongodb, on rails 3.

Update and upgrade the system
-------------------------------

    sudo apt-get update
    sudo apt-get upgrade

Emacs
-----

    sudo apt-get install emacs

DNS
---

Point DNS as correct IP

Installing git
----------------

    sudo apt-get install git-core

Check out code

Enterprise Ruby
---

Go to:
http://www.rubyenterpriseedition.com/download.html

    sudo dpkg -i ruby-enterprise_1.8.7-2010.01_i386.deb

(or install from source)


Firewall Setup
--------------

    Install ipkungfu
    Configure

MongoDB
-------

    Install MongoDB 
    http://t.pitale.com/posts/mongodb-in-a-deployed-environment.html

Configure timezone
-------------------

    sudo dpkg-reconfigure tzdata
    sudo apt-get install ntp
    sudo ntpdate ntp.ubuntu.com # Update time
    
Verify that you have to correct date and time with

    date

Configure hostname
-------------------

    sudo hostname your-hostname

Add 127.0.0.1 your-hostname

    sudo emacs /etc/hosts
    
Write your-hostname in 
    
    sudo emacs /etc/hostname
    
Verify that hostname is set
    
    hostname

Apache 
-------

I tried to install nginx, but was not successful. I found it frustrating and opaque. http://serverfault.com/questions/133536/how-do-i-troubleshoot-nginx-not-recognizing-passenger

    sudo gem install passenger
    sudo passenger-install-apache-module

    sudo gem update --system

