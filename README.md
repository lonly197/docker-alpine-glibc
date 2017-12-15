# docker-alpine-glibc

[![](https://images.microbadger.com/badges/image/lonly/docker-alpine-glibc.svg)](http://microbadger.com/images/lonly/alpine-glibc)

> This image is based on Alpine Linux image, which is only a 5MB image, and contains glibc to enable
proprietary projects compiled against glibc (e.g. OracleJDK, Anaconda) work on Alpine.

## Introduction

> Please use corresponding branches from this repo to play with code.

- __2.26-r0 = 2.26 = 2 = latest__

This image includes some quirks to make [glibc](https://www.gnu.org/software/libc/) work side by
side with musl libc (default in Apline Linux). glibc packages for Alpine Linux are prepared by
[Andy Shinn](https://github.com/andyshinn) and the releases are published in
[andyshinn/alpine-pkg-glibc](https://github.com/andyshinn/alpine-pkg-glibc) github repo.

## Usage

This image is intended to be a base image for your projects, so you may use it like this:

```Dockerfile
FROM lonly/docker-alpine-glibc

COPY ./my_app /usr/local/bin/my_app
```

```sh
$ docker build -t my_app .
```

There are already several images using this image, so you can refer to them as usage examples:

* [`lonly/docker-alpine-oraclejdk8`](https://hub.docker.com/r/lonly/docker-alpine-oraclejdk8/) ([github](https://github.com/lonly197/docker-alpine-oraclejdk8))


## License

![License](https://img.shields.io/github/license/lonly197/docker-alpine-glibc.svg)

## Contact me

- Email: <lonly197@qq.com>