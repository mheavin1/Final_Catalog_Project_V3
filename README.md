# Catalog App readme file hello from readme

This project creates a Catalog Application that allows users to view sprorting goods items, login to the app, make new items and edit existing items.

## Getting Started

These instructions will list the IP Address, URL, summary of software installed and summary of configurations made for the deployment of the catalog app on an Amazon Lightstail instance.

The catalog app display a sports catalog, with a Google login feature.

IP address: 13.59.201.43

URL: http://13.59.201.43.xip.io



### Summary of Software installed on my Amazon Lightsail instance:

update and upgrade: 
sudo apt-get update
sudo apt-get upgrade

other installations:
ntp, apache2, libapache2-mod-wsgi, postgresql, postgresql-contrib, git, virtualenv, python-pip, 

Installations for Pyton: flask, httplib2, oauth2client, sqlalchemy, psycopg2, packaging, oauth2client, redis, passlib, flask-httpauth, flask-sqlalchemy, bleach, requests


### Summary of configurations on my Amazon Lightsail instance:

Added a new user named grader, and gave grader sudo access.

Disable password authentication: /etc/ssh/sshd_config: confirmed the following is no:  PasswordAuthentication no

Root login disabled.

Changed SSH Port to 2200:
   -  Added the Custom rule in Lightsail dashboard firewall, TCP protocol, Port 2200
   -  edited /etc/ssh/sshd_config, changed the port to 2200
   
Configured firewall to allow for NTP on port 123:  sudo ufw allow 123/udp
Setup UFW:
  - udo ufw default deny incoming
  - sudo ufw default allow outgoing
  - sudo ufw allow ssh
  - sudo ufw allow 2200/tcp (Note: Changed SSH above to port 2200)
  - sudo ufw allow www
  - sudo ufw allow 123/udp
  - sudo ufw enable






### And coding style tests

Coding style tests were completed with PEP8 online Check.

Example: http://pep8online.com/checkresult


## Built With

* [Python IDLE editor](https://www.python.org/downloads/) - The editor used
* Notepadd ++ for editing CSS and Html files.

## Versioning

Version 1

## Authors

* Marc


