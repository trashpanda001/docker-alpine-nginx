### Alpine Linux Nginx

A lightweight [Nginx][nginx] [Docker image][dockerhub_project] built from source atop [Alpine Linux][alpine_linux]. Available on [GitHub][github_project].

Tags with the `-k8s` suffix are built on [Alpine-Kubernetes][alpine_kubernetes], an image for Kubernetes and other Docker cluster environments that use DNS-based service discovery. It adds the necessary `search` domain support for DNS resolution.

#### Mainline 1.11.x Branch Tags

* `1.11.0`, `1.11`, `mainline`, `latest` (2016-05-24, [Dockerfile][dockerfile_1_11], [Changes][nginx_changes])
* `1.11.0-k8s`, `1.11-k8s`, `mainline-k8s`, `latest-k8s` ([Dockerfile][dockerfile_1_11_k8s] for Kubernetes)

#### Stable 1.10.x Branch Tags

* `1.10.0`, `1.10`, `stable` (2016-04-26, [Dockerfile][dockerfile_1_10], [Changes][nginx_changes_1_10])
* `1.10.0-k8s`, `1.10-k8s`, `stable-k8s` ([Dockerfile][dockerfile_1_10_k8s] for Kubernetes)

#### Old Mainline 1.9.x Branch Tags

* `1.9.15`, `1.9.15-k8s`, `1.9`, `1.9-k8s` (2016-04-19)
* `1.9.14`, `1.9.14-k8s` (2016-04-05)
* `1.9.13`, `1.9.13-k8s` (2016-03-29)
* `1.9.12`, `1.9.12-k8s` (2016-02-24)
* `1.9.11`, `1.9.11-k8s` (2016-02-09)
* `1.9.10`, `1.9.10-k8s` (2016-01-26)
* `1.9.9` (2015-12-09)
* `1.9.8` (2015-12-08)
* `1.9.7` (2015-11-17)

#### Legacy 1.8.x Branch Tags

* `1.8.1`, `1.8`, `legacy` (2016-01-26, [Dockerfile][dockerfile_1_8], [Changes][nginx_changes_1_8])
* `1.8.1-k8s`, `1.8-k8s`, `legacy-k8s` ([Dockerfile][dockerfile_1_8_k8s] for Kubernetes)

### Default Usage

```bash
$ docker run --rm sickp/alpine-nginx:1.11.0 # nginx -g "daemon off;"
2016/05/25 16:05:50 [notice] 1#1: using the "epoll" event method
2016/05/25 16:05:50 [notice] 1#1: nginx/1.11.0
2016/05/25 16:05:50 [notice] 1#1: built by gcc 5.3.0 (Alpine 5.3.0)
2016/05/25 16:05:50 [notice] 1#1: OS: Linux 4.1.19-boot2docker
2016/05/25 16:05:50 [notice] 1#1: getrlimit(RLIMIT_NOFILE): 1048576:1048576
2016/05/25 16:05:50 [notice] 1#1: start worker processes
2016/05/25 16:05:50 [notice] 1#1: start worker process 5
```

### Configuration

[Nginx][nginx] is compiled from source using the same [configure arguments][nginx_configure] as the official, pre-built packages.

```bash
$ docker run --rm sickp/alpine-nginx:1.11.0 nginx -V
nginx version: nginx/1.11.0
built by gcc 5.3.0 (Alpine 5.3.0)
built with OpenSSL 1.0.2h  3 May 2016
TLS SNI support enabled
configure arguments: --prefix=/etc/nginx --sbin-path=/usr/sbin/nginx --conf-path=/etc/nginx/nginx.conf --error-log-path=/var/log/nginx/error.log --http-log-path=/var/log/nginx/access.log --pid-path=/var/run/nginx.pid --lock-path=/var/run/nginx.lock --http-client-body-temp-path=/var/cache/nginx/client_temp --http-proxy-temp-path=/var/cache/nginx/proxy_temp --http-fastcgi-temp-path=/var/cache/nginx/fastcgi_temp --http-uwsgi-temp-path=/var/cache/nginx/uwsgi_temp --http-scgi-temp-path=/var/cache/nginx/scgi_temp --user=nginx --group=nginx --with-http_ssl_module --with-http_realip_module --with-http_addition_module --with-http_sub_module --with-http_dav_module --with-http_flv_module --with-http_mp4_module --with-http_gunzip_module --with-http_gzip_static_module --with-http_random_index_module --with-http_secure_link_module --with-http_stub_status_module --with-http_auth_request_module --with-threads --with-stream --with-stream_ssl_module --with-http_slice_module --with-mail --with-mail_ssl_module --with-file-aio --with-http_v2_module --with-ipv6

$ docker run --rm -it sickp/alpine-nginx:1.11.0 openssl version
OpenSSL 1.0.2h  3 May 2016

$ docker run --rm sickp/alpine-nginx:1.11.0 cat /etc/alpine-release
3.3.3
```

### History

- 2016-05-25 - Added new mainline branch Nginx 1.11.0, OpenSSL 1.0.2h.
- 2016-04-26 - Added new stable branch Nginx 1.10.0. Moved old stable to legacy branch. Added more `-k8s` tags.
- 2016-04-21 - Updated to Nginx 1.9.15.
- 2016-04-05 - Updated to Nginx 1.9.14, Alpine Linux 3.3.3. Added stable branch Nginx 1.8.1.
- 2016-03-30 - Updated to Nginx 1.9.13, OpenSSL 1.0.2g.
- 2016-02-24 - Updated to Nginx 1.9.12.
- 2016-02-09 - Updated to Nginx 1.9.11 (and added http_slice_module).
- 2016-02-09 - Updated to OpenSSL 1.0.2f. Added support for ALPINE_NO_RESOLVER in 1.9.10-k8s.
- 2016-01-27 - Added Kubernetes versions (-k8s), until Alpine Linux/musl adds DNS search support.
- 2016-01-26 - Updated to Nginx 1.9.10, Alpine Linux 3.3.1.
- 2015-12-24 - Updated 1.9.9 image to Alpine Linux 3.3 (gcc 5.3.0, OpenSSL 1.0.2e).
- 2015-12-10 - Updated to 1.9.9.
- 2015-11-27 - Initial version.

[alpine_kubernetes]:   https://hub.docker.com/r/janeczku/alpine-kubernetes/
[alpine_linux]:        https://hub.docker.com/_/alpine/
[dockerhub_project]:   https://hub.docker.com/r/sickp/alpine-nginx/
[dockerfile_1_8]:      https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.8.1/Dockerfile
[dockerfile_1_8_k8s]:  https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.8.1-k8s/Dockerfile
[dockerfile_1_10]:     https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.10.0/Dockerfile
[dockerfile_1_10_k8s]: https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.10.0-k8s/Dockerfile
[dockerfile_1_11]:     https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.11.0/Dockerfile
[dockerfile_1_11_k8s]: https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.11.0-k8s/Dockerfile
[github_project]:      https://github.com/sickp/docker-alpine-nginx/
[nginx]:               http://nginx.org/
[nginx_changes]:       http://nginx.org/en/CHANGES
[nginx_changes_1_8]:   http://nginx.org/en/CHANGES-1.8
[nginx_changes_1_10]:  http://nginx.org/en/CHANGES-1.10
[nginx_configure]:     http://nginx.org/en/linux_packages.html#mainline
