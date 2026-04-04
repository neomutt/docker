FROM debian:sid-slim

ENV DEBIAN_FRONTEND=noninteractive

RUN \
	apt update && \
	apt upgrade -y && \
	ln -fs /usr/share/zoneinfo/Europe/London /etc/localtime && \
	apt install -y \
		ccache \
		docbook-simple \
		docbook-xsl \
		gcc \
		gettext \
		git \
		gpgsm \
		jimsh \
		libgdbm-dev \
		libgnutls28-dev \
		libgpgme-dev \
		libgsasl-dev \
		libgss-dev \
		libidn2-dev \
		libkrb5-dev \
		liblmdb-dev \
		liblua5.2-dev \
		liblz4-dev \
		libncurses-dev \
		libnotmuch-dev \
		libpcre2-dev \
		librocksdb-dev \
		libsasl2-dev \
		libsqlite3-dev \
		libssl-dev \
		libtdb-dev \
		libxml2-utils \
		libzstd-dev \
		lua5.2 \
		lynx \
		make \
		mandoc \
		tzdata \
		w3m \
		xsltproc && \
	dpkg-reconfigure --frontend noninteractive tzdata && \
	apt autoclean && \
	apt autoremove
