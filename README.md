# Docker Images

<div style="float: right;">
<a href="https://github.com/neomutt/docker-build/actions/workflows/build.yml"><img src="https://github.com/neomutt/docker-build/actions/workflows/build.yml/badge.svg" /></a>
<a href="https://github.com/neomutt/docker-build/actions/workflows/centos.yml"><img src="https://github.com/neomutt/docker-build/actions/workflows/centos.yml/badge.svg" /></a>
<a href="https://github.com/neomutt/docker-build/actions/workflows/fedora.yml"><img src="https://github.com/neomutt/docker-build/actions/workflows/fedora.yml/badge.svg" /></a>
</div>

The basic Docker image used by [GitHub Actions](https://docs.github.com/en/actions)
is very minimal.  In order to fully build and test NeoMutt, we need to install
lots of development packages.  This takes time and lots of bandwidth.

To speed up the builds, we create Docker images containing a full development
environment.

The main tests are done in an Ubuntu 20.04 (latest) environment.  
We also perform weekly tests under Centos and Fedora.

## Building

The images are built by more GitHub Actions:

- [build.yml](.github/workflows/build.yml) -- Ubuntu 20.04
- [centos.yml](.github/workflows/centos.yml) -- Centos 7, 8
- [fedora.yml](.github/workflows/fedora.yml) -- Fedora 34, 35, 36 (rawhide)

Each Action is scheduled to run automaticaly on the 1<sup>st</sup> of the month at 3am.  
This will ensure we have up-to-date packages for every environment.

The builds are defined by Dockerfiles:

| Dockerfile                               | Description         |
| :--------------------------------------- | :------------------ |
| [Dockerfile](Dockerfile)                 | Ubuntu 20.04        |
| [Dockerfile.centos7](Dockerfile.centos7) | Centos 7 / RHEL 7   |
| [Dockerfile.centos8](Dockerfile.centos8) | Centos 8 / RHEL 8   |
| [Dockerfile.f34](Dockerfile.f34)         | Fedora 34           |
| [Dockerfile.f35](Dockerfile.f35)         | Fedora 35           |
| [Dockerfile.f36](Dockerfile.f36)         | Fedora 36 (rawhide) |

