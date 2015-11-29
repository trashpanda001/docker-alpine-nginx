### Alpine Linux Nginx

An [Nginx][nginx] [Docker image][alpine_nginx] built on top of [Glider Labs's Alpine Linux][gliderlabs_alpine] Docker image.


#### Supported tags and `Dockerfile` links

* [`1.9.7`][dockerfile_1_9], [`1.9`][dockerfile_1_9], [`mainline`][dockerfile_1_9], [`latest`][dockerfile_1_9] ([Dockerfile][dockerfile_1_9])


### Configuration

[Nginx][nginx] is compiled from source using the same [configure arguments][nginx_configure] as the official, pre-built packages.

```ash
$ nginx -V
```

```
nginx version: nginx/1.9.7
built by gcc 4.9.2 (Alpine 4.9.2)
built with OpenSSL 1.0.2d 9 Jul 2015
TLS SNI support enabled
configure arguments:
  --prefix=/etc/nginx
  --sbin-path=/usr/sbin/nginx
  --conf-path=/etc/nginx/nginx.conf
  --error-log-path=/var/log/nginx/error.log
  --http-log-path=/var/log/nginx/access.log
  --pid-path=/var/run/nginx.pid
  --lock-path=/var/run/nginx.lock
  --http-client-body-temp-path=/var/cache/nginx/client_temp
  --http-proxy-temp-path=/var/cache/nginx/proxy_temp
  --http-fastcgi-temp-path=/var/cache/nginx/fastcgi_temp
  --http-uwsgi-temp-path=/var/cache/nginx/uwsgi_temp
  --http-scgi-temp-path=/var/cache/nginx/scgi_temp
  --user=nginx
  --group=nginx
  --with-http_ssl_module
  --with-http_realip_module
  --with-http_addition_module
  --with-http_sub_module
  --with-http_dav_module
  --with-http_flv_module
  --with-http_mp4_module
  --with-http_gunzip_module
  --with-http_gzip_static_module
  --with-http_random_index_module
  --with-http_secure_link_module
  --with-http_stub_status_module
  --with-http_auth_request_module
  --with-mail
  --with-mail_ssl_module
  --with-file-aio
  --with-ipv6
  --with-threads
  --with-stream
  --with-stream_ssl_module
  --with-http_v2_module
```

### History

- 2015-11-27 Initial version.

[alpine_nginx]:      https://hub.docker.com/r/sickp/alpine-nginx/
[gliderlabs_alpine]: https://hub.docker.com/r/gliderlabs/alpine/
[dockerfile_1_9]:    https://github.com/sickp/docker-alpine-nginx/tree/master/Dockerfile
[nginx]:             http://nginx.org/
[nginx_configure]:   http://nginx.org/en/linux_packages.html#mainline
