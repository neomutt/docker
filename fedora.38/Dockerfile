# Create a NeoMutt development environment based on Fedora 38
FROM fedora:38

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
		kyotocabinet-devel \
		lcov \
		libdb-devel \
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
		qdbm-devel \
		redhat-rpm-config \
		rocksdb-devel \
		rsync \
		slang-devel \
		sqlite \
		sqlite-devel \
		tar \
		tcl \
		tokyocabinet-devel \
		w3m

# vim: syn=dockerfile
