# termux-nginx

Precompiled NginX binary for running in [Termux/Android](https://termux.com)

![screenshot](https://raw.githubusercontent.com/andrwj/termux-nginx/master/screenshot-nexus5.png)


Compiled options
-----------------
```bash
./configure \
  --prefix=/data/data/com.termux/files/usr/share/nginx \
  --pid-path=/data/data/com.termux/files/usr/var/run/nginx.pid \
  --lock-path=/data/data/com.termux/files/usr/var/log/nginx.lock \
  --http-log-path=/data/data/com.termux/files/usr/var/log/nginx/access.log \
  --with-http_ssl_module \
  --with-stream \
  --with-compat
```



Installation
------------

Copy .tgz file into termux and extract on `/data/data/com.termux/files/usr/share/`. Don't forget to make `log` directory.

```sh
$ cd
$ mkdir -p ../usr/var/log/nginx
$ cd ../usr/share/
$ tar xvfz nginx-v1.11.5-termux.tgz
$ ls -F ./nginx/
client_body_temp/  conf/  fastcgi_temp/  html/  logs/  proxy_temp/  sbin/  scgi_temp/  uwsgi_temp/
$ cd ./nginx/sbin/
$ ./nginx -V
nginx version: nginx/1.11.5
built with OpenSSL 1.0.2j  26 Sep 2016
TLS SNI support enabled
configure arguments: --prefix=/data/data/com.termux/files/usr/share/nginx --pid-path=/data/data/com.termux/files/usr/var/run/nginx.pid --lock-path=/data/data/com.termux/files/usr/var/log/nginx.lock --http-log-path=/data/data/com.termux/files/usr/var/log/nginx/access.log --with-http_ssl_module --with-stream --with-compat
```

	
nginx version
-------------
v1.11.5

Compiled at Nov. 12 2016 by [@andrwj](http://twitter.com/andrwj)
