# Create a NeoMutt development environment based on Fedora 43
FROM fedora:43

RUN \
	dnf clean all && \
	dnf -y update && \
	dnf install -y \
		ccache \
		clang \
		clang-tools-extra \
		cyrus-sasl-devel \
		docbook-dtds \
		docbook-style-xsl \
		doxygen \
		elinks \
		gcc \
		gdbm-devel \
		gettext-devel \
		git \
		gnutls-devel \
		gpgme-devel \
		graphviz \
		iwyu \
		jq \
		krb5-devel \
		lcov \
		libgsasl-devel \
		libidn-devel \
		libtdb-devel \
		libxslt \
		libzstd-devel \
		lmdb-devel \
		lua \
		lua-devel \
		lynx \
		lz4-devel \
		ncurses-devel \
		notmuch-devel \
		openssl-devel \
		pcre2-devel \
		redhat-rpm-config \
		rocksdb-devel \
		rsync \
		sqlite \
		sqlite-devel \
		tar \
		tcl \
		w3m

# vim: syn=dockerfile
