# Docker Images

<div style="float: right;">
<a href="https://github.com/neomutt/docker-build/actions/workflows/build.yml"><img src="https://github.com/neomutt/docker-build/actions/workflows/build.yml/badge.svg" /></a>
<a href="https://github.com/neomutt/docker-build/actions/workflows/fedora.yml"><img src="https://github.com/neomutt/docker-build/actions/workflows/fedora.yml/badge.svg" /></a>
</div>

The basic Docker image used by [GitHub Actions](https://docs.github.com/en/actions)
is very minimal.  In order to fully build and test NeoMutt, we need to install
lots of development packages.  This takes time and lots of bandwidth.

To speed up the builds, we create Docker images containing a full development
environment.

The main tests are done in an Ubuntu 22.04 (latest) environment.  
We also perform weekly tests under Fedora.

## Building

The images are built by more GitHub Actions:

- [build.yml](.github/workflows/build.yml) -- Ubuntu 22.04
- [fedora.yml](.github/workflows/fedora.yml) -- Fedora 37, 38, 39 (rawhide)

Each Action is scheduled to run automaticaly on the 1<sup>st</sup> of the month at 3am.  
This will ensure we have up-to-date packages for every environment.

The builds are defined by Dockerfiles:

| Dockerfile                               | Description         |
| :--------------------------------------- | :------------------ |
| [Dockerfile](Dockerfile)                 | Ubuntu 22.04        |
| [Dockerfile.f37](Dockerfile.f37)         | Fedora 37           |
| [Dockerfile.f38](Dockerfile.f38)         | Fedora 38           |
| [Dockerfile.f39](Dockerfile.f39)         | Fedora 39 (rawhide) |

