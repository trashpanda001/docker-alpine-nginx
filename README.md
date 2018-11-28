### Alpine Linux Nginx

A lightweight [Nginx][nginx] [Docker image][docker_project] built from source atop [Alpine Linux][alpine_linux]. It is compiled from source using the same [configure arguments][nginx_configure] as the official, pre-built packages. Available on [GitHub][github_project].

    $ docker run --rm sickp/alpine-nginx:1.15.7-r1  # nginx -g 'daemon off';

The version tag format is formed from the Nginx version `{major}.{minor}.{teeny}` plus an image revision `-r{revision}`. The image revision will change if the Dockerfile or Alpine base image changes.

### Mainline - `1.15.7-r1`, `1.15.7`, `1.15`, `mainline`, `latest`

[Dockerfile](https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.15.6-r1/Dockerfile) / [ChangeLog][nginx_changes] / 2018-11-06

    $ docker run --rm sickp/alpine-nginx:1.15.7-r1 about
    * Nginx 1.15.7
    built by gcc 6.4.0 (Alpine 6.4.0) 
    built with LibreSSL 2.7.4
    TLS SNI support enabled
    configure arguments: --prefix=/etc/nginx --sbin-path=/usr/sbin/nginx --conf-path=/etc/nginx/nginx.conf --error-log-path=/var/log/nginx/error.log --pid-path=/var/run/nginx.pid --lock-path=/var/run/nginx.lock --user=nginx --group=nginx --with-threads --with-file-aio --with-http_ssl_module --with-http_v2_module --with-http_realip_module --with-http_addition_module --with-http_sub_module --with-http_dav_module --with-http_flv_module --with-http_mp4_module --with-http_gunzip_module --with-http_gzip_static_module --with-http_auth_request_module --with-http_random_index_module --with-http_secure_link_module --with-http_slice_module --with-http_stub_status_module --http-log-path=/var/log/nginx/access.log --http-client-body-temp-path=/var/cache/nginx/client_temp --http-proxy-temp-path=/var/cache/nginx/proxy_temp --http-fastcgi-temp-path=/var/cache/nginx/fastcgi_temp --http-uwsgi-temp-path=/var/cache/nginx/uwsgi_temp --http-scgi-temp-path=/var/cache/nginx/scgi_temp --with-mail --with-mail_ssl_module --with-stream --with-stream_ssl_module --with-stream_realip_module
    * Alpine Linux 3.8.1

#### 1.15.x Tags

| Tag        | Version | Date       | Alpine | LibreSSL |
| ---------- | ------- | ---------- | ------ | -------- |
| 1.15.7-r1  | 1.15.7  | 2018-11-27 | 3.8.1  | 2.7.4    |
| 1.15.6-r1  | 1.15.6  | 2018-11-06 | 3.8.1  | 2.7.4    |
| 1.15.5-r1  | 1.15.5  | 2018-10-02 | 3.8.1  | 2.7.4    |
| 1.15.4-r1  | 1.15.4  | 2018-09-25 | 3.8.1  | 2.7.4    |
| 1.15.3-r1  | 1.15.3  | 2018-08-28 | 3.8.1  | 2.7.4    |
| 1.15.2-r1  | 1.15.2  | 2018-07-24 | 3.8.1  | 2.7.4    |
| 1.15.1-r1  | 1.15.1  | 2018-07-03 | 3.7.0  | 2.6.5    |
| 1.15.0-r1  | 1.15.0  | 2018-06-05 | 3.7.0  | 2.6.5    |

### Stable - `1.14.1-r1`, `1.14.1`, `1.14`, `stable`

[Dockerfile](https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.14.0-r1/Dockerfile) / [ChangeLog][nginx_changes_1_14] / 2018-11-06

    $ docker run --rm sickp/alpine-nginx:1.14.1-r1 about
    * Nginx 1.14.1
    built by gcc 6.4.0 (Alpine 6.4.0) 
    built with LibreSSL 2.7.4
    TLS SNI support enabled
    configure arguments: --prefix=/etc/nginx --sbin-path=/usr/sbin/nginx --conf-path=/etc/nginx/nginx.conf --error-log-path=/var/log/nginx/error.log --pid-path=/var/run/nginx.pid --lock-path=/var/run/nginx.lock --user=nginx --group=nginx --with-threads --with-file-aio --with-http_ssl_module --with-http_v2_module --with-http_realip_module --with-http_addition_module --with-http_sub_module --with-http_dav_module --with-http_flv_module --with-http_mp4_module --with-http_gunzip_module --with-http_gzip_static_module --with-http_auth_request_module --with-http_random_index_module --with-http_secure_link_module --with-http_slice_module --with-http_stub_status_module --http-log-path=/var/log/nginx/access.log --http-client-body-temp-path=/var/cache/nginx/client_temp --http-proxy-temp-path=/var/cache/nginx/proxy_temp --http-fastcgi-temp-path=/var/cache/nginx/fastcgi_temp --http-uwsgi-temp-path=/var/cache/nginx/uwsgi_temp --http-scgi-temp-path=/var/cache/nginx/scgi_temp --with-mail --with-mail_ssl_module --with-stream --with-stream_ssl_module --with-stream_realip_module
    * Alpine Linux 3.8.1

#### 1.14.x Tags

| Tag        | Version | Date       | Alpine | LibreSSL |
| ---------- | ------- | ---------- | ------ | -------- |
| 1.14.1-r1  | 1.14.1  | 2018-11-06 | 3.8.1  | 2.7.4    |
| 1.14.0-r1  | 1.14.0  | 2018-04-17 | 3.7.0  | 2.6.3    |

### Mainline - `1.13.12-r1`, `1.13.12`, `1.13`, `mainline`, `latest`

[Dockerfile](https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.13.12-r1/Dockerfile) / [ChangeLog][nginx_changes] / 2018-04-10

    $ docker run --rm sickp/alpine-nginx:1.13.12-r1 about
    * Nginx 1.13.12
    built by gcc 6.4.0 (Alpine 6.4.0) 
    built with LibreSSL 2.6.3
    TLS SNI support enabled
    configure arguments: --prefix=/etc/nginx --sbin-path=/usr/sbin/nginx --conf-path=/etc/nginx/nginx.conf --error-log-path=/var/log/nginx/error.log --http-log-path=/var/log/nginx/access.log --pid-path=/var/run/nginx.pid --lock-path=/var/run/nginx.lock --http-client-body-temp-path=/var/cache/nginx/client_temp --http-proxy-temp-path=/var/cache/nginx/proxy_temp --http-fastcgi-temp-path=/var/cache/nginx/fastcgi_temp --http-uwsgi-temp-path=/var/cache/nginx/uwsgi_temp --http-scgi-temp-path=/var/cache/nginx/scgi_temp --user=nginx --group=nginx --with-http_ssl_module --with-http_realip_module --with-http_addition_module --with-http_sub_module --with-http_dav_module --with-http_flv_module --with-http_mp4_module --with-http_gunzip_module --with-http_gzip_static_module --with-http_random_index_module --with-http_secure_link_module --with-http_stub_status_module --with-http_auth_request_module --with-threads --with-stream --with-stream_ssl_module --with-http_slice_module --with-mail --with-mail_ssl_module --with-file-aio --with-http_v2_module --with-ipv6 --with-stream_realip_module
    * Alpine Linux 3.7.0

#### 1.13.x Tags

| Tag        | Version | Date       | Alpine | LibreSSL |
| ---------- | ------- | ---------- | ------ | -------- |
| 1.13.12-r1 | 1.13.12 | 2018-04-10 | 3.7.0  | 2.6.3    |
| 1.13.11-r1 | 1.13.11 | 2018-04-03 | 3.7.0  | 2.6.3    |
| 1.13.10-r1 | 1.13.10 | 2018-03-21 | 3.7.0  | 2.6.3    |
| 1.13.9-r1  | 1.13.9  | 2018-02-20 | 3.7.0  | 2.6.3    |
| 1.13.8-r1  | 1.13.8  | 2017-12-26 | 3.7.0  | 2.6.3    |
| 1.13.7-r2  | 1.13.7  | 2017-11-21 | 3.7.0  | 2.6.3    |
| 1.13.7-r1  | 1.13.7  | 2017-11-21 | 3.6.2  | 2.5.5    |
| 1.13.6-r1  | 1.13.6  | 2017-10-10 | 3.6.2  | 2.5.5    |
| 1.13.5-r1  | 1.13.5  | 2017-09-05 | 3.6.2  | 2.5.4    |
| 1.13.4-r1  | 1.13.4  | 2017-08-08 | 3.6.2  | 2.5.4    |
| 1.13.3-r1  | 1.13.3  | 2017-07-11 | 3.6.2  | 2.5.4    |
| 1.13.2-r1  | 1.13.2  | 2017-06-27 | 3.6.2  | 2.5.4    |
| 1.13.1-r1  | 1.13.1  | 2017-05-30 | 3.6.0  | 2.5.4    |
| 1.13.0-r1  | 1.13.0  | 2017-04-25 | 3.5.2  | 2.4.4    |

### Old Stable - `1.12.2-r2`, `1.12.2`, `1.12`

[Dockerfile](https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.12.2-r2/Dockerfile) / [ChangeLog][nginx_changes_1_12] / 2017-10-17

    $ docker run --rm sickp/alpine-nginx:1.12.2-r2 about
    * Nginx 1.12.2
    built by gcc 6.4.0 (Alpine 6.4.0) 
    built with LibreSSL 2.6.3
    TLS SNI support enabled
    configure arguments: --prefix=/etc/nginx --sbin-path=/usr/sbin/nginx --conf-path=/etc/nginx/nginx.conf --error-log-path=/var/log/nginx/error.log --http-log-path=/var/log/nginx/access.log --pid-path=/var/run/nginx.pid --lock-path=/var/run/nginx.lock --http-client-body-temp-path=/var/cache/nginx/client_temp --http-proxy-temp-path=/var/cache/nginx/proxy_temp --http-fastcgi-temp-path=/var/cache/nginx/fastcgi_temp --http-uwsgi-temp-path=/var/cache/nginx/uwsgi_temp --http-scgi-temp-path=/var/cache/nginx/scgi_temp --user=nginx --group=nginx --with-http_ssl_module --with-http_realip_module --with-http_addition_module --with-http_sub_module --with-http_dav_module --with-http_flv_module --with-http_mp4_module --with-http_gunzip_module --with-http_gzip_static_module --with-http_random_index_module --with-http_secure_link_module --with-http_stub_status_module --with-http_auth_request_module --with-threads --with-stream --with-stream_ssl_module --with-http_slice_module --with-mail --with-mail_ssl_module --with-file-aio --with-http_v2_module --with-ipv6 --with-stream_realip_module
    * Alpine Linux 3.7.0

#### 1.12.x Tags

| Tag        | Version | Date       | Alpine | LibreSSL |
| ---------- | ------- | ---------- | ------ | -------- |
| 1.12.2-r2  | 1.12.2  | 2017-10-17 | 3.7.0  | 2.6.3    |
| 1.12.2-r1  | 1.12.2  | 2017-10-17 | 3.6.2  | 2.5.5    |
| 1.12.1-r1  | 1.12.1  | 2017-07-11 | 3.6.2  | 2.5.4    |
| 1.12.0-r2  | 1.12.0  | 2017-04-12 | 3.6.0  | 2.5.4    |
| 1.12.0-r1  | 1.12.0  | 2017-04-12 | 3.5.2  | 2.4.4    |

### Old Mainline - `1.11.13-r1`, `1.11.13`, `1.11`

[Dockerfile](https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.11.13-r1/Dockerfile) / [ChangeLog][nginx_changes] / 2017-04-04

    $ docker run --rm sickp/alpine-nginx:1.11.13-r1 about
    * Nginx 1.11.13
    built by gcc 6.2.1 20160822 (Alpine 6.2.1)
    built with LibreSSL 2.4.4
    TLS SNI support enabled
    configure arguments: --prefix=/etc/nginx --sbin-path=/usr/sbin/nginx --conf-path=/etc/nginx/nginx.conf --error-log-path=/var/log/nginx/error.log --http-log-path=/var/log/nginx/access.log --pid-path=/var/run/nginx.pid --lock-path=/var/run/nginx.lock --http-client-body-temp-path=/var/cache/nginx/client_temp --http-proxy-temp-path=/var/cache/nginx/proxy_temp --http-fastcgi-temp-path=/var/cache/nginx/fastcgi_temp --http-uwsgi-temp-path=/var/cache/nginx/uwsgi_temp --http-scgi-temp-path=/var/cache/nginx/scgi_temp --user=nginx --group=nginx --with-http_ssl_module --with-http_realip_module --with-http_addition_module --with-http_sub_module --with-http_dav_module --with-http_flv_module --with-http_mp4_module --with-http_gunzip_module --with-http_gzip_static_module --with-http_random_index_module --with-http_secure_link_module --with-http_stub_status_module --with-http_auth_request_module --with-threads --with-stream --with-stream_ssl_module --with-http_slice_module --with-mail --with-mail_ssl_module --with-file-aio --with-http_v2_module --with-ipv6 --with-stream_realip_module
    * Alpine Linux 3.5.2

#### 1.11.x Tags

| Tag        | Version | Date       | Alpine | LibreSSL |
| ---------- | ------- | ---------- | ------ | -------- |
| 1.11.13-r1 | 1.11.13 | 2017-04-04 | 3.5.2  | 2.4.4    |
| 1.11.12-r1 | 1.11.12 | 2017-03-24 | 3.5.2  | 2.4.4    |
| 1.11.11-r1 | 1.11.11 | 2017-03-21 | 3.5.2  | 2.4.4    |
| 1.11.10    | 1.11.10 | 2017-02-14 |        |          |
| 1.11.9     | 1.11.9  | 2017-01-24 |        |          |
| 1.11.8     | 1.11.8  | 2016-12-27 |        |          |
| 1.11.7     | 1.11.7  | 2016-12-13 |        |          |
| 1.11.6     | 1.11.6  | 2016-11-15 |        |          |
| 1.11.5     | 1.11.5  | 2016-10-11 |        |          |
| 1.11.4     | 1.11.4  | 2016-09-13 |        |          |
| 1.11.3     | 1.11.3  | 2016-07-26 |        |          |
| 1.11.2     | 1.11.2  | 2016-07-05 |        |          |
| 1.11.1     | 1.11.1  | 2016-05-31 |        |          |
| 1.11.0     | 1.11.0  | 2016-05-24 |        |          |

### Really Old Stable - `1.10.3-r2`, `1.10.3`, `1.10`

[Dockerfile](https://github.com/sickp/docker-alpine-nginx/tree/master/versions/1.10.3-r2/Dockerfile) / [ChangeLog][nginx_changes_1_10] / 2017-03-21

    $ docker run --rm sickp/alpine-nginx:1.10.3-r2 about
    * Nginx 1.10.3
    built by gcc 6.2.1 20160822 (Alpine 6.2.1)
    built with LibreSSL 2.4.4
    TLS SNI support enabled
    configure arguments: --prefix=/etc/nginx --sbin-path=/usr/sbin/nginx --conf-path=/etc/nginx/nginx.conf --error-log-path=/var/log/nginx/error.log --http-log-path=/var/log/nginx/access.log --pid-path=/var/run/nginx.pid --lock-path=/var/run/nginx.lock --http-client-body-temp-path=/var/cache/nginx/client_temp --http-proxy-temp-path=/var/cache/nginx/proxy_temp --http-fastcgi-temp-path=/var/cache/nginx/fastcgi_temp --http-uwsgi-temp-path=/var/cache/nginx/uwsgi_temp --http-scgi-temp-path=/var/cache/nginx/scgi_temp --user=nginx --group=nginx --with-http_ssl_module --with-http_realip_module --with-http_addition_module --with-http_sub_module --with-http_dav_module --with-http_flv_module --with-http_mp4_module --with-http_gunzip_module --with-http_gzip_static_module --with-http_random_index_module --with-http_secure_link_module --with-http_stub_status_module --with-http_auth_request_module --with-threads --with-stream --with-stream_ssl_module --with-http_slice_module --with-mail --with-mail_ssl_module --with-file-aio --with-http_v2_module --with-ipv6
    * Alpine Linux 3.5.2

#### 1.10.x Tags

| Tag        | Version | Date       | Alpine | LibreSSL |
| ---------- | ------- | ---------- | ------ | -------- |
| 1.10.3-r2  | 1.10.3  | 2017-03-21 | 3.5.2  | 2.4.4    |
| 1.10.2     | 1.10.2  | 2016-10-18 |        |          |
| 1.10.1     | 1.10.1  | 2016-05-31 |        |          |
| 1.10.0     | 1.10.0  | 2016-04-26 |        |          |

[alpine_linux]:        https://store.docker.com/images/alpine
[docker_project]:      https://store.docker.com/community/images/sickp/alpine-nginx
[github_project]:      https://github.com/sickp/docker-alpine-nginx/
[nginx]:               http://nginx.org/
[nginx_changes]:       http://nginx.org/en/CHANGES
[nginx_changes_1_10]:  http://nginx.org/en/CHANGES-1.10
[nginx_changes_1_12]:  http://nginx.org/en/CHANGES-1.12
[nginx_changes_1_14]:  http://nginx.org/en/CHANGES-1.14
[nginx_configure]:     http://nginx.org/en/linux_packages.html#mainline
