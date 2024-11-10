FROM ubuntu:24.04

ENV DEBIAN_FRONTEND=noninteractive

RUN \
	apt update && \
	apt upgrade -y && \
	ln -fs /usr/share/zoneinfo/Europe/London /etc/localtime && \
	apt install -y \
		autopoint \
		ccache \
		clang \
		cmake \
		curl \
		docbook-simple \
		docbook-xsl \
		doxygen \
		gettext \
		git \
		gpgsm \
		graphviz \
		jimsh \
		lcov \
		libasan6 \
		libclang-dev \
		libdb-dev \
		libfuzzer-14-dev \
		libgdbm-dev \
		libgnutls28-dev \
		libgpgme11-dev \
		libgsasl7-dev \
		libgss-dev \
		libidn2-0-dev \
		libkrb5-dev \
		libkyotocabinet-dev \
		liblmdb-dev \
		liblua5.2-dev \
		liblz4-dev \
		libncursesw5-dev \
		libnotmuch-dev \
		libpcre2-dev \
		libqdbm-dev \
		librocksdb-dev \
		libsasl2-dev \
		libslang2-dev \
		libsqlite3-dev \
		libssl-dev \
		libtdb-dev \
		libtokyocabinet-dev \
		libunwind-dev \
		libxml2-utils \
		libzstd-dev \
		llvm-dev \
		lua5.2 \
		lynx \
		make \
		rsync \
		tzdata \
		w3m \
		wget \
		xsltproc && \
	dpkg-reconfigure --frontend noninteractive tzdata && \
	apt autoclean && \
	apt autoremove

