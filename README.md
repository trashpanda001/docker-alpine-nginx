### Alpine Linux Nginx

A lightweight [Nginx][nginx] [Docker image][alpine_nginx] built atop [Alpine Linux][gliderlabs_alpine]. Available on [GitHub][github_project].

Tags with the `-k8s` suffix are built on [Alpine-Kubernetes][alpine_kubernetes], an image for Kubernetes and other Docker cluster environments that use DNS-based service discovery. It adds the necessary `search` domain support for DNS resolution.


#### Tags

* [`1.9.10`][dockerfile_1_9_10], [`1.9`][dockerfile_1_9_10], [`mainline`][dockerfile_1_9_10], [`latest`][dockerfile_1_9_10] (2016-01-26, [Changes][nginx_changes])
* [`1.9.10-k8s`][dockerfile_1_9_10_k8s] (for Kubernetes)
* [`1.9.9`][dockerfile_1_9_9] (2015-12-09)
* [`1.9.8`][dockerfile_1_9_8] (2015-12-08)
* [`1.9.7`][dockerfile_1_9_7] (2015-11-17)


### Configuration

[Nginx][nginx] is compiled from source using the same [configure arguments][nginx_configure] as the official, pre-built packages.

```sh
$ docker run --rm sickp/alpine-nginx:latest -V
nginx version: nginx/1.9.10
built by gcc 5.3.0 (Alpine 5.3.0)
built with OpenSSL 1.0.2e 3 Dec 2015
TLS SNI support enabled
configure arguments:
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

docker run --rm --entrypoint=cat sickp/alpine-nginx:latest /etc/alpine-release
3.3.1
```

### History

- 2016-01-27 Added Kubernetes versions (-k8s), until Alpine Linux/musl adds DNS search support.
- 2016-01-26 Updated to Nginx 1.9.10, Alpine Linux 3.3.1.
- 2015-12-24 Updated 1.9.9 image to Alpine Linux 3.3 (gcc 5.3.0, OpenSSL 1.0.2e).
- 2015-12-10 Updated to 1.9.9.
- 2015-11-27 Initial version.

[alpine_kubernetes]:     https://hub.docker.com/r/janeczku/alpine-kubernetes/
[alpine_nginx]:          https://hub.docker.com/r/sickp/alpine-nginx/
[github_project]:        https://github.com/sickp/docker-alpine-nginx/
[gliderlabs_alpine]:     https://hub.docker.com/r/gliderlabs/alpine/
[dockerfile_1_9_10]:     https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.9.10/Dockerfile
[dockerfile_1_9_10_k8s]: https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.9.10-k8s/Dockerfile
[dockerfile_1_9_9]:      https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.9.9/Dockerfile
[dockerfile_1_9_8]:      https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.9.8/Dockerfile
[dockerfile_1_9_7]:      https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.9.7/Dockerfile
[nginx]:                 http://nginx.org/
[nginx_changes]:         http://nginx.org/en/CHANGES
[nginx_configure]:       http://nginx.org/en/linux_packages.html#mainline
