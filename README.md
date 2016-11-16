### Alpine Linux Nginx

A lightweight [Nginx][nginx] [Docker image][dockerhub_project] built from source atop [Alpine Linux][alpine_linux]. Available on [GitHub][github_project].

> If you're running Kubernetes 1.2.0 or later on all your cluster nodes, you should now use the non-`k8s` tags below. These tags are built on Alpine Linux 3.4, which adds the necessary DNS search support for service discovery. Kubernetes defaults to `dnsPolicy=ClusterFirst` in pod specs, and defines a single `nameserver` in `/etc/resolv.conf`. This means things should finally work correctly for Alpine Linux images without modification.

#### Mainline 1.11.x Branch Tags

- `1.11.6`, `1.11`, `mainline`, `latest` (2016-11-15, [Dockerfile](https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.11.6/Dockerfile), [Changes][nginx_changes])
- `1.11.5` (2016-10-11)
- `1.11.4` (2016-09-13)
- `1.11.3` (2016-07-26)
- `1.11.2` (2016-07-05)
- `1.11.1` (2016-05-31)
- `1.11.0` (2016-05-24)

#### Stable 1.10.x Branch Tags

- `1.10.2`, `1.10`, `stable` (2016-10-18, [Dockerfile](https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.10.2/Dockerfile), [Changes][nginx_changes_1_10])
- `1.10.1` (2016-05-31)
- `1.10.0` (2016-04-26)

#### Legacy 1.8.x Branch Tags

- `1.8.1`, `1.8`, `legacy` (2016-01-26, [Dockerfile](https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.8.1/Dockerfile), [Changes][nginx_changes_1_8])

#### Kubernetes <1.2.0

Tags with the `-k8s` suffix are built on [Alpine-Kubernetes 3.3][alpine_kubernetes], an image for Kubernetes and other Docker cluster environments that use DNS-based service discovery. It adds the necessary `search` domain support for DNS resolution.

 - `1.11.1-k8s`, `1.11-k8s`, `mainline-k8s`, `latest-k8s`
 - `1.11.0-k8s`
 - `1.10.1-k8s`, `1.10-k8s`, `stable-k8s`
 - `1.10.0-k8s`
 - `1.8.1-k8s`, `1.8-k8s`, `legacy-k8s`

### Default Usage

```bash
$ docker run --rm sickp/alpine-nginx:1.11.6
2016/11/16 02:01:17 [notice] 1#1: using the "epoll" event method
2016/11/16 02:01:17 [notice] 1#1: nginx/1.11.6
2016/11/16 02:01:17 [notice] 1#1: built by gcc 5.3.0 (Alpine 5.3.0)
2016/11/16 02:01:17 [notice] 1#1: OS: Linux 4.4.27-moby
2016/11/16 02:01:17 [notice] 1#1: getrlimit(RLIMIT_NOFILE): 1048576:1048576
2016/11/16 02:01:17 [notice] 1#1: start worker processes
2016/11/16 02:01:17 [notice] 1#1: start worker process 6
```

### Configuration

[Nginx][nginx] is compiled from source using the same [configure arguments][nginx_configure] as the official, pre-built packages.

```bash
$ docker run --rm sickp/alpine-nginx:1.11.6 nginx -V
nginx version: nginx/1.11.6
built by gcc 5.3.0 (Alpine 5.3.0)
built with OpenSSL 1.0.2j  26 Sep 2016
TLS SNI support enabled
configure arguments: --prefix=/etc/nginx --sbin-path=/usr/sbin/nginx --conf-path=/etc/nginx/nginx.conf --error-log-path=/var/log/nginx/error.log --http-log-path=/var/log/nginx/access.log --pid-path=/var/run/nginx.pid --lock-path=/var/run/nginx.lock --http-client-body-temp-path=/var/cache/nginx/client_temp --http-proxy-temp-path=/var/cache/nginx/proxy_temp --http-fastcgi-temp-path=/var/cache/nginx/fastcgi_temp --http-uwsgi-temp-path=/var/cache/nginx/uwsgi_temp --http-scgi-temp-path=/var/cache/nginx/scgi_temp --user=nginx --group=nginx --with-http_ssl_module --with-http_realip_module --with-http_addition_module --with-http_sub_module --with-http_dav_module --with-http_flv_module --with-http_mp4_module --with-http_gunzip_module --with-http_gzip_static_module --with-http_random_index_module --with-http_secure_link_module --with-http_stub_status_module --with-http_auth_request_module --with-threads --with-stream --with-stream_ssl_module --with-http_slice_module --with-mail --with-mail_ssl_module --with-file-aio --with-http_v2_module --with-ipv6

$ docker run --rm -it sickp/alpine-nginx:1.11.6 openssl version
OpenSSL 1.0.2j  26 Sep 2016

$ docker run --rm sickp/alpine-nginx:1.11.6 cat /etc/alpine-release
3.4.4
```

### History

- 2016-11-16 - Updated to Nginx 1.11.6 (Alpine Linux 3.4.4).
- 2016-10-18 - Added Nginx 1.10.2 (OpenSSL 1.0.2j, Alpine Linux 3.4.4).
- 2016-10-11 - Updated to Nginx 1.11.5 (OpenSSL 1.0.2j, Alpine Linux 3.4.3).
- 2016-09-13 - Updated to Nginx 1.11.4.
- 2016-07-26 - Updated to Nginx 1.11.3.
- 2016-07-11 - Updated to Nginx 1.11.2.
- 2016-06-15 - Updated 1.11.x, 1.10.x, 1.8.x to Alpine Linux 3.4.0 (with `search` support for Kubernetes >=1.2.0).
- 2016-06-01 - Updated to Nginx 1.11.1 (mainline) and Nginx 1.10.1 (stable).
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
[github_project]:      https://github.com/sickp/docker-alpine-nginx/
[nginx]:               http://nginx.org/
[nginx_changes]:       http://nginx.org/en/CHANGES
[nginx_changes_1_8]:   http://nginx.org/en/CHANGES-1.8
[nginx_changes_1_10]:  http://nginx.org/en/CHANGES-1.10
[nginx_configure]:     http://nginx.org/en/linux_packages.html#mainline
