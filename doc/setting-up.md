Configuring NNTPChan server
===========================

This document provides a step-by-step guide to configurin your NNTPChan node.

##Configuring via web-interface (WIP)

You can configure NNTPChan via the web-interface by navigating your browser to http://127.0.0.1:18000.

###Selecting your data-storage system

![Image 1](http://i.imgur.com/l9iiXxB.png)

First your will be asked what data-storage system you would like to use. We support Redis and PostgreSQL.

<hr>

####Redis configuration

![Image 2](http://i.imgur.com/HDp4Ddf.png)

If you have chosen Redis then fill in the fields below:

* **Hostname or IP Address** - This is the hostname or IP address of your Redis server (I would run it locally on 127.0.0.1 to be safe).
* **Port number** - The port that your Redis server is running on.
* **Password** - Optional authentication password for Redis ([Setting up a Redis password](securing-redis.md)).

<hr>

####PostgreSQL configuration

![Image 3](http://i.imgur.com/WPXedZB.png)

If you have chosen PostgreSQL then fill in the fields below:

* **Hostname or IP Address** - This is the hostname or IP address of your PostreSQL server (I would run it locally on 127.0.0.1 to be safe). 
* **Port number** - This is the port that your PostgreSQL server is running on.
* **Username** - The username for PostgreSQL.
* **Password** - The password for PostgreSQL.

<hr>

###Configuring the NNTP server

![Image 4](http://i.imgur.com/FXxShtu.png)

Fill in the fields required for the NNTP server.

* **Name of NNTP instance** - What is the significamce of this name.
* **Allow attachements** - Check the box if you want people to be able to add attachements to posts.
* **Allow anonymous posters** - Check the box if you want to allow anonymous posters.
* **Allow attachments from anonymous posters** - Check the box if you want to allow anonymous posters to add attachments to their posts.
* **Require TLS for incoming connections** - Check the box if NNTP connections must be encrypted and authenticated with TLS (highly recommended).

###Configuring TLS

![Image 5](http://i.imgur.com/EjkrjTT.png)

Fill in the fields required for the TLS security system.

* **Hostname or IP address** - FIXME.
* **TLS keyname** - FIXME.

###Set paths to external programs

![Image 6](http://i.imgur.com/hBXYJDo.png)

NNTPChan needs to know the paths to the listed programs on your system.

* **convert path** - Path to the `convert` program.
* **ffmpeg path** - Path to the `ffmpeg` program.
* **sox path** - Path to the `sox` program.

##Manual configuration (WIP)

FIXME
