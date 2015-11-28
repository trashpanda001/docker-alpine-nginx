### Alpine Linux Nginx

An [Nginx container][alpine_nginx] built on top of [Glider Labs's Alpine Linux][gliderlabs_alpine] Docker image.

Nginx is compiled from source using the same [configure arguments][nginx_configure] Nginx's pre-built packages use.


#### Supported tags and `Dockerfile` links

* [`1.9.7`][dockerfile_1_9], [`1.9`][dockerfile_1_9], [`mainline`][dockerfile_1_9], [`latest`][dockerfile_1_9] (Alpine Linux 3.2.x, Nginx 1.9.7)


### History

- 2015-11-27 Initial version.

[alpine_nginx]:      https://hub.docker.com/r/sickp/alpine-nginx/
[gliderlabs_alpine]: https://hub.docker.com/r/gliderlabs/alpine/
[dockerfile_1_9]:    https://github.com/sickp/docker-alpine-nginx/tree/master/Dockerfile
[nginx_configure]:   http://nginx.org/en/linux_packages.html#mainline
