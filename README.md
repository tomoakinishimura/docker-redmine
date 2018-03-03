# Introduction

Dockerfile to build a [Redmine](http://www.redmine.org/) container image.

## Version

Current Version: **sameersbn/redmine:3.4.4-2**

*P.S.: If your installation depends on various third party plugins, please stick with 2.6.xx series to avoid breakage.*

# Contributing

If you find this image useful here's how you can help:

- Send a Pull Request with your awesome new features and bug fixes
- Help new users with [Issues](https://github.com/sameersbn/docker-redmine/issues) they may encounter
- Support the development of this image with a [donation](http://www.damagehead.com/donate/)

# Issues

Docker is a relatively new project and is active being developed and tested by a thriving community of developers and testers and every release of docker features many enhancements and bugfixes.

Given the nature of the development and release cycle it is very important that you have the latest version of docker installed because any issue that you encounter might have already been fixed with a newer docker release.

Install the most recent version of the Docker Engine for your platform using the [official Docker releases](http://docs.docker.com/engine/installation/), which can also be installed using:

```bash
wget -qO- https://get.docker.com/ | sh
```

Fedora and RHEL/CentOS users should try disabling selinux with `setenforce 0` and check if resolves the issue. If it does than there is not much that I can help you with. You can either stick with selinux disabled (not recommended by redhat) or switch to using ubuntu.

If using the latest docker version and/or disabling selinux does not fix the issue then please file a issue request on the [issues](https://github.com/sameersbn/docker-redmine/issues) page.

In your issue report please make sure you provide the following information:

- The host distribution and release version.
- Output of the `docker version` command.
- Output of the `docker info` command.
- The `docker run` command you used to run the image (mask out the sensitive bits).

# Installation

Automated builds of the image are available on [Dockerhub](https://hub.docker.com/r/sameersbn/redmine) and is the recommended method of installation.

> **Note**: Builds are also available on [Quay.io](https://quay.io/repository/sameersbn/redmine)

```bash
docker pull sameersbn/redmine:latest
```

Since version `2.4.2`, the image builds are being tagged. You can now pull a particular version of redmine by specifying the version number. For example,

```bash
docker pull sameersbn/redmine:3.4.4-2
```

Alternately you can build the image yourself.

```bash
docker build -t sameersbn/redmine github.com/sameersbn/docker-redmine
```

# Quick Start

The quickest way to get started is using [docker-compose](https://docs.docker.com/compose/).

```bash
wget https://raw.githubusercontent.com/sameersbn/docker-redmine/master/docker-compose.yml
docker-compose up
```
