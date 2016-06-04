`srnd.ini`
==========

`srnd.ini` is the configuration file for your NNTPChan node. Some configuration can be done initially through the web-interface (for now hopefully) but there is more that can be done by tweaking your `srnd.ini` file.

Below is the default state of the file. We will explain each section below.

````
[nntp]
instance_name=test.srndv2.tld
bind=127.0.0.1:1199
sync_on_start=1
allow_anon=0
allow_anon_attachments=0
allow_attachments=1
require_tls=1
anon_nntp=0

[pprof]
enable=0
bind=127.0.0.1:17000

[crypto]
tls-keyname=overchan
tls-hostname=!!put-hostname-or-ip-of-server-here
tls-trust-dir=certs

[articles]
store_dir=articles
incoming_dir=/tmp/articles
attachments_dir=webroot/img
thumbs_dir=webroot/thm
convert_bin=/usr/bin/convert
ffmpegthumbnailer_bin=/usr/bin/ffmpeg
sox_bin=/usr/bin/sox
compression=0

[database]
type=redis
schema=single
host=localhost
port=6379
user
password

[cache]
type=file

[frontend]
enable=1
allow_files=1
regen_on_start=0
regen_threads=1
bind=[::]:18000
name=web.srndv2.test
webroot=webroot
prefix=/
static_files=contrib
templates=contrib/templates/default
translations=contrib/translations
locale=en
domain=localhost
json-api=0
json-api-username=fucking-change-this-value
json-api-password=seriously-fucking-change-this-value
api-secret=RTZP5JZ2XGYCY===
````

##`[nntp]`

All NNTP server-related settings.

####instance_name

This is the name for your NNTP server. I don't really know what the point of it is, but hey its there (FIXME).

####bind

This is where you put the address and port that you would like the NNTP server to run on where `x` is the address and `y` is the port in `bind=x:y`.

####sync_on_start

* When this is set to `1` your NNTP server will sync articles with its peers on startup.
* When this is set to `0` then no syncing will take place on statup.

####allow_anon

* When this is set to `1` bluh.
* When this is set to `0` bluh.

####allow_anon_attachments

* When this is set to `1` bluh.
* When this is set to `0` bluh.

####allow_attachments

* When this is set to `1` posters my attach images to their posts.
* When this is set to `0` posters may not attach images to their posts.

####require_tls

* When this is set to `1` then any NNTP connection to this server will need to use TLS.
* When this is set to `0` then any NNTP connection to this server will not need to use TLS (but it could? - FIXME)

####anon_nntp

* When this is set to `1` bluh.
* When this is set to `0` bluh.

##`[pprof]`

All pprof-related settings.

####enable

* When this is set to `1` bluh.
* When this is set to `0` bluh.

####bind

FIXME
