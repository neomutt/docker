# Docker Images

<div style="float: right;">
<a href="https://github.com/neomutt/docker/actions/workflows/ubuntu.yml"><img src="https://github.com/neomutt/docker/actions/workflows/ubuntu.yml/badge.svg" /></a>
<a href="https://github.com/neomutt/docker/actions/workflows/fedora.yml"><img src="https://github.com/neomutt/docker/actions/workflows/fedora.yml/badge.svg" /></a>
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

- [ubuntu.yml](.github/workflows/ubuntu.yml) -- Ubuntu 22.04
- [fedora.yml](.github/workflows/fedora.yml) -- Fedora 38, 39, 40 (rawhide)

Each Action is scheduled to run automaticaly on the 1<sup>st</sup> of the month at 3am.  
This will ensure we have up-to-date packages for every environment.

The builds are defined by Dockerfiles:

| Dockerfile                                         | Description         |
| :------------------------------------------------- | :------------------ |
| [ubuntu.22.04/Dockerfile](ubuntu.22.04/Dockerfile) | Ubuntu 22.04        |
| [fedora.38/Dockerfile](fedora.38/Dockerfile)       | Fedora 38           |
| [fedora.39/Dockerfile](fedora.39/Dockerfile)       | Fedora 39           |
| [fedora.40/Dockerfile](fedora.40/Dockerfile)       | Fedora 40 (rawhide) |





