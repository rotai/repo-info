<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `celery`

-	[`celery:4.0.2`](#celery402)
-	[`celery:4.0`](#celery40)
-	[`celery:4`](#celery4)
-	[`celery:3.1.25`](#celery3125)
-	[`celery:3.1`](#celery31)
-	[`celery:3`](#celery3)
-	[`celery:latest`](#celerylatest)

## `celery:4.0.2`

```console
$ docker pull celery@sha256:53cc71cadcd6b769ffc88e994cbffba74cd61fa64d25181f5d9db8443b2e289a
```

-	Platforms:
	-	linux; amd64

### `celery:4.0.2` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80483794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaf223f42b661ec5ad5a9c524d875f62ff6dc0dfbb05ccffdc2e9c31d4da1bb`
-	Default Command: `["celery","worker"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 20:40:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 20:40:14 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 22:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:31:10 GMT
ENV GPG_KEY=97FC712E4C024BBEA48A61ED3A5CA953F73C700D
# Tue, 28 Feb 2017 22:36:58 GMT
ENV PYTHON_VERSION=3.5.3
# Tue, 28 Feb 2017 22:36:58 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 28 Feb 2017 22:38:48 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libgdbm-dev 		liblzma-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-loadable-sqlite-extensions 		--enable-shared 	&& make -j$(nproc) 	&& make install 	&& ldconfig 		&& if [ ! -e /usr/local/bin/pip3 ]; then : 		&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python3 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	; fi 	&& pip3 install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 28 Feb 2017 22:38:49 GMT
RUN cd /usr/local/bin 	&& { [ -e easy_install ] || ln -s easy_install-* easy_install; } 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 28 Feb 2017 22:38:49 GMT
CMD ["python3"]
# Wed, 01 Mar 2017 01:45:11 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Wed, 01 Mar 2017 01:45:11 GMT
WORKDIR /home/user
# Wed, 01 Mar 2017 01:45:16 GMT
RUN pip install redis
# Wed, 01 Mar 2017 01:45:24 GMT
ENV CELERY_VERSION=4.0.2
# Wed, 01 Mar 2017 01:45:27 GMT
RUN pip install celery=="$CELERY_VERSION"
# Wed, 01 Mar 2017 01:45:28 GMT
RUN { 	echo 'import os'; 	echo "BROKER_URL = os.environ.get('CELERY_BROKER_URL', 'amqp://')"; } > celeryconfig.py
# Wed, 01 Mar 2017 01:45:28 GMT
ENV CELERY_BROKER_URL=amqp://guest@rabbit
# Wed, 01 Mar 2017 01:45:29 GMT
USER [user]
# Wed, 01 Mar 2017 01:45:29 GMT
CMD ["celery" "worker"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764f950e58321d40da999d0b1da856017c3b0faecaf1f6b02c228b7c854ac450`  
		Last Modified: Wed, 01 Mar 2017 15:55:20 GMT  
		Size: 3.3 MB (3344487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7929bfadb7abb12cab2fbe98cecd4bf9e76ac1798a91ae0724306ef92382b19f`  
		Last Modified: Wed, 01 Mar 2017 16:08:02 GMT  
		Size: 21.0 MB (20951735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8b59f20dbc72d93c9922c6ebd4e951d9bf553ea7174b47a3ffab15c5410228`  
		Last Modified: Wed, 01 Mar 2017 16:07:50 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3da70a026a508593be13faa499639ffe0f9cf32461d38bf1f758f11abf3e9c`  
		Last Modified: Wed, 01 Mar 2017 22:52:15 GMT  
		Size: 4.3 KB (4346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e0e7f8761108192c0298a9a8250b85523d27d2148f01aa26a080b2c8e9ee74`  
		Last Modified: Wed, 01 Mar 2017 22:52:17 GMT  
		Size: 1.8 MB (1849021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb535c12f30f659d7d269ab0e7eb521e5bf2a47840062f1adf815ebd0112819`  
		Last Modified: Wed, 01 Mar 2017 22:53:32 GMT  
		Size: 3.0 MB (2970334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff15c4a90553f6d82e9c507c3ae75602df4d19abff58e6f787dd0c09c74be92`  
		Last Modified: Wed, 01 Mar 2017 22:53:30 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `celery:4.0`

```console
$ docker pull celery@sha256:53cc71cadcd6b769ffc88e994cbffba74cd61fa64d25181f5d9db8443b2e289a
```

-	Platforms:
	-	linux; amd64

### `celery:4.0` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80483794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaf223f42b661ec5ad5a9c524d875f62ff6dc0dfbb05ccffdc2e9c31d4da1bb`
-	Default Command: `["celery","worker"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 20:40:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 20:40:14 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 22:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:31:10 GMT
ENV GPG_KEY=97FC712E4C024BBEA48A61ED3A5CA953F73C700D
# Tue, 28 Feb 2017 22:36:58 GMT
ENV PYTHON_VERSION=3.5.3
# Tue, 28 Feb 2017 22:36:58 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 28 Feb 2017 22:38:48 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libgdbm-dev 		liblzma-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-loadable-sqlite-extensions 		--enable-shared 	&& make -j$(nproc) 	&& make install 	&& ldconfig 		&& if [ ! -e /usr/local/bin/pip3 ]; then : 		&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python3 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	; fi 	&& pip3 install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 28 Feb 2017 22:38:49 GMT
RUN cd /usr/local/bin 	&& { [ -e easy_install ] || ln -s easy_install-* easy_install; } 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 28 Feb 2017 22:38:49 GMT
CMD ["python3"]
# Wed, 01 Mar 2017 01:45:11 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Wed, 01 Mar 2017 01:45:11 GMT
WORKDIR /home/user
# Wed, 01 Mar 2017 01:45:16 GMT
RUN pip install redis
# Wed, 01 Mar 2017 01:45:24 GMT
ENV CELERY_VERSION=4.0.2
# Wed, 01 Mar 2017 01:45:27 GMT
RUN pip install celery=="$CELERY_VERSION"
# Wed, 01 Mar 2017 01:45:28 GMT
RUN { 	echo 'import os'; 	echo "BROKER_URL = os.environ.get('CELERY_BROKER_URL', 'amqp://')"; } > celeryconfig.py
# Wed, 01 Mar 2017 01:45:28 GMT
ENV CELERY_BROKER_URL=amqp://guest@rabbit
# Wed, 01 Mar 2017 01:45:29 GMT
USER [user]
# Wed, 01 Mar 2017 01:45:29 GMT
CMD ["celery" "worker"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764f950e58321d40da999d0b1da856017c3b0faecaf1f6b02c228b7c854ac450`  
		Last Modified: Wed, 01 Mar 2017 15:55:20 GMT  
		Size: 3.3 MB (3344487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7929bfadb7abb12cab2fbe98cecd4bf9e76ac1798a91ae0724306ef92382b19f`  
		Last Modified: Wed, 01 Mar 2017 16:08:02 GMT  
		Size: 21.0 MB (20951735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8b59f20dbc72d93c9922c6ebd4e951d9bf553ea7174b47a3ffab15c5410228`  
		Last Modified: Wed, 01 Mar 2017 16:07:50 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3da70a026a508593be13faa499639ffe0f9cf32461d38bf1f758f11abf3e9c`  
		Last Modified: Wed, 01 Mar 2017 22:52:15 GMT  
		Size: 4.3 KB (4346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e0e7f8761108192c0298a9a8250b85523d27d2148f01aa26a080b2c8e9ee74`  
		Last Modified: Wed, 01 Mar 2017 22:52:17 GMT  
		Size: 1.8 MB (1849021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb535c12f30f659d7d269ab0e7eb521e5bf2a47840062f1adf815ebd0112819`  
		Last Modified: Wed, 01 Mar 2017 22:53:32 GMT  
		Size: 3.0 MB (2970334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff15c4a90553f6d82e9c507c3ae75602df4d19abff58e6f787dd0c09c74be92`  
		Last Modified: Wed, 01 Mar 2017 22:53:30 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `celery:4`

```console
$ docker pull celery@sha256:53cc71cadcd6b769ffc88e994cbffba74cd61fa64d25181f5d9db8443b2e289a
```

-	Platforms:
	-	linux; amd64

### `celery:4` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80483794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaf223f42b661ec5ad5a9c524d875f62ff6dc0dfbb05ccffdc2e9c31d4da1bb`
-	Default Command: `["celery","worker"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 20:40:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 20:40:14 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 22:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:31:10 GMT
ENV GPG_KEY=97FC712E4C024BBEA48A61ED3A5CA953F73C700D
# Tue, 28 Feb 2017 22:36:58 GMT
ENV PYTHON_VERSION=3.5.3
# Tue, 28 Feb 2017 22:36:58 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 28 Feb 2017 22:38:48 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libgdbm-dev 		liblzma-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-loadable-sqlite-extensions 		--enable-shared 	&& make -j$(nproc) 	&& make install 	&& ldconfig 		&& if [ ! -e /usr/local/bin/pip3 ]; then : 		&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python3 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	; fi 	&& pip3 install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 28 Feb 2017 22:38:49 GMT
RUN cd /usr/local/bin 	&& { [ -e easy_install ] || ln -s easy_install-* easy_install; } 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 28 Feb 2017 22:38:49 GMT
CMD ["python3"]
# Wed, 01 Mar 2017 01:45:11 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Wed, 01 Mar 2017 01:45:11 GMT
WORKDIR /home/user
# Wed, 01 Mar 2017 01:45:16 GMT
RUN pip install redis
# Wed, 01 Mar 2017 01:45:24 GMT
ENV CELERY_VERSION=4.0.2
# Wed, 01 Mar 2017 01:45:27 GMT
RUN pip install celery=="$CELERY_VERSION"
# Wed, 01 Mar 2017 01:45:28 GMT
RUN { 	echo 'import os'; 	echo "BROKER_URL = os.environ.get('CELERY_BROKER_URL', 'amqp://')"; } > celeryconfig.py
# Wed, 01 Mar 2017 01:45:28 GMT
ENV CELERY_BROKER_URL=amqp://guest@rabbit
# Wed, 01 Mar 2017 01:45:29 GMT
USER [user]
# Wed, 01 Mar 2017 01:45:29 GMT
CMD ["celery" "worker"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764f950e58321d40da999d0b1da856017c3b0faecaf1f6b02c228b7c854ac450`  
		Last Modified: Wed, 01 Mar 2017 15:55:20 GMT  
		Size: 3.3 MB (3344487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7929bfadb7abb12cab2fbe98cecd4bf9e76ac1798a91ae0724306ef92382b19f`  
		Last Modified: Wed, 01 Mar 2017 16:08:02 GMT  
		Size: 21.0 MB (20951735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8b59f20dbc72d93c9922c6ebd4e951d9bf553ea7174b47a3ffab15c5410228`  
		Last Modified: Wed, 01 Mar 2017 16:07:50 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3da70a026a508593be13faa499639ffe0f9cf32461d38bf1f758f11abf3e9c`  
		Last Modified: Wed, 01 Mar 2017 22:52:15 GMT  
		Size: 4.3 KB (4346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e0e7f8761108192c0298a9a8250b85523d27d2148f01aa26a080b2c8e9ee74`  
		Last Modified: Wed, 01 Mar 2017 22:52:17 GMT  
		Size: 1.8 MB (1849021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb535c12f30f659d7d269ab0e7eb521e5bf2a47840062f1adf815ebd0112819`  
		Last Modified: Wed, 01 Mar 2017 22:53:32 GMT  
		Size: 3.0 MB (2970334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff15c4a90553f6d82e9c507c3ae75602df4d19abff58e6f787dd0c09c74be92`  
		Last Modified: Wed, 01 Mar 2017 22:53:30 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `celery:3.1.25`

```console
$ docker pull celery@sha256:913d240525291580bee19f45e52e0e534b549567d4af73612e0e6d22160f7e20
```

-	Platforms:
	-	linux; amd64

### `celery:3.1.25` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81750893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144dc6bd2859dff3952a2310aaed138a6bd245f9a108fcd0ea5061bafe697122`
-	Default Command: `["celery","worker"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 20:40:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 20:40:14 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 22:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:31:10 GMT
ENV GPG_KEY=97FC712E4C024BBEA48A61ED3A5CA953F73C700D
# Tue, 28 Feb 2017 22:36:58 GMT
ENV PYTHON_VERSION=3.5.3
# Tue, 28 Feb 2017 22:36:58 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 28 Feb 2017 22:38:48 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libgdbm-dev 		liblzma-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-loadable-sqlite-extensions 		--enable-shared 	&& make -j$(nproc) 	&& make install 	&& ldconfig 		&& if [ ! -e /usr/local/bin/pip3 ]; then : 		&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python3 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	; fi 	&& pip3 install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 28 Feb 2017 22:38:49 GMT
RUN cd /usr/local/bin 	&& { [ -e easy_install ] || ln -s easy_install-* easy_install; } 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 28 Feb 2017 22:38:49 GMT
CMD ["python3"]
# Wed, 01 Mar 2017 01:45:11 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Wed, 01 Mar 2017 01:45:11 GMT
WORKDIR /home/user
# Wed, 01 Mar 2017 01:45:16 GMT
RUN pip install redis
# Wed, 01 Mar 2017 01:45:16 GMT
ENV CELERY_VERSION=3.1.25
# Wed, 01 Mar 2017 01:45:22 GMT
RUN pip install celery=="$CELERY_VERSION"
# Wed, 01 Mar 2017 01:45:23 GMT
RUN { 	echo 'import os'; 	echo "BROKER_URL = os.environ.get('CELERY_BROKER_URL', 'amqp://')"; } > celeryconfig.py
# Wed, 01 Mar 2017 01:45:23 GMT
ENV CELERY_BROKER_URL=amqp://guest@rabbit
# Wed, 01 Mar 2017 01:45:23 GMT
USER [user]
# Wed, 01 Mar 2017 01:45:24 GMT
CMD ["celery" "worker"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764f950e58321d40da999d0b1da856017c3b0faecaf1f6b02c228b7c854ac450`  
		Last Modified: Wed, 01 Mar 2017 15:55:20 GMT  
		Size: 3.3 MB (3344487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7929bfadb7abb12cab2fbe98cecd4bf9e76ac1798a91ae0724306ef92382b19f`  
		Last Modified: Wed, 01 Mar 2017 16:08:02 GMT  
		Size: 21.0 MB (20951735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8b59f20dbc72d93c9922c6ebd4e951d9bf553ea7174b47a3ffab15c5410228`  
		Last Modified: Wed, 01 Mar 2017 16:07:50 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3da70a026a508593be13faa499639ffe0f9cf32461d38bf1f758f11abf3e9c`  
		Last Modified: Wed, 01 Mar 2017 22:52:15 GMT  
		Size: 4.3 KB (4346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e0e7f8761108192c0298a9a8250b85523d27d2148f01aa26a080b2c8e9ee74`  
		Last Modified: Wed, 01 Mar 2017 22:52:17 GMT  
		Size: 1.8 MB (1849021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123afa2ec3b970bb05181661689a6d99edf03a4cd1acba5fa4791195c3e8840e`  
		Last Modified: Wed, 01 Mar 2017 22:52:18 GMT  
		Size: 4.2 MB (4237430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa0d7142d0e0f8954aee117b21ba3778ed12c9c4b8813a5f80e01ab9140e030`  
		Last Modified: Wed, 01 Mar 2017 22:52:16 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `celery:3.1`

```console
$ docker pull celery@sha256:913d240525291580bee19f45e52e0e534b549567d4af73612e0e6d22160f7e20
```

-	Platforms:
	-	linux; amd64

### `celery:3.1` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81750893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144dc6bd2859dff3952a2310aaed138a6bd245f9a108fcd0ea5061bafe697122`
-	Default Command: `["celery","worker"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 20:40:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 20:40:14 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 22:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:31:10 GMT
ENV GPG_KEY=97FC712E4C024BBEA48A61ED3A5CA953F73C700D
# Tue, 28 Feb 2017 22:36:58 GMT
ENV PYTHON_VERSION=3.5.3
# Tue, 28 Feb 2017 22:36:58 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 28 Feb 2017 22:38:48 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libgdbm-dev 		liblzma-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-loadable-sqlite-extensions 		--enable-shared 	&& make -j$(nproc) 	&& make install 	&& ldconfig 		&& if [ ! -e /usr/local/bin/pip3 ]; then : 		&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python3 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	; fi 	&& pip3 install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 28 Feb 2017 22:38:49 GMT
RUN cd /usr/local/bin 	&& { [ -e easy_install ] || ln -s easy_install-* easy_install; } 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 28 Feb 2017 22:38:49 GMT
CMD ["python3"]
# Wed, 01 Mar 2017 01:45:11 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Wed, 01 Mar 2017 01:45:11 GMT
WORKDIR /home/user
# Wed, 01 Mar 2017 01:45:16 GMT
RUN pip install redis
# Wed, 01 Mar 2017 01:45:16 GMT
ENV CELERY_VERSION=3.1.25
# Wed, 01 Mar 2017 01:45:22 GMT
RUN pip install celery=="$CELERY_VERSION"
# Wed, 01 Mar 2017 01:45:23 GMT
RUN { 	echo 'import os'; 	echo "BROKER_URL = os.environ.get('CELERY_BROKER_URL', 'amqp://')"; } > celeryconfig.py
# Wed, 01 Mar 2017 01:45:23 GMT
ENV CELERY_BROKER_URL=amqp://guest@rabbit
# Wed, 01 Mar 2017 01:45:23 GMT
USER [user]
# Wed, 01 Mar 2017 01:45:24 GMT
CMD ["celery" "worker"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764f950e58321d40da999d0b1da856017c3b0faecaf1f6b02c228b7c854ac450`  
		Last Modified: Wed, 01 Mar 2017 15:55:20 GMT  
		Size: 3.3 MB (3344487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7929bfadb7abb12cab2fbe98cecd4bf9e76ac1798a91ae0724306ef92382b19f`  
		Last Modified: Wed, 01 Mar 2017 16:08:02 GMT  
		Size: 21.0 MB (20951735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8b59f20dbc72d93c9922c6ebd4e951d9bf553ea7174b47a3ffab15c5410228`  
		Last Modified: Wed, 01 Mar 2017 16:07:50 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3da70a026a508593be13faa499639ffe0f9cf32461d38bf1f758f11abf3e9c`  
		Last Modified: Wed, 01 Mar 2017 22:52:15 GMT  
		Size: 4.3 KB (4346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e0e7f8761108192c0298a9a8250b85523d27d2148f01aa26a080b2c8e9ee74`  
		Last Modified: Wed, 01 Mar 2017 22:52:17 GMT  
		Size: 1.8 MB (1849021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123afa2ec3b970bb05181661689a6d99edf03a4cd1acba5fa4791195c3e8840e`  
		Last Modified: Wed, 01 Mar 2017 22:52:18 GMT  
		Size: 4.2 MB (4237430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa0d7142d0e0f8954aee117b21ba3778ed12c9c4b8813a5f80e01ab9140e030`  
		Last Modified: Wed, 01 Mar 2017 22:52:16 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `celery:3`

```console
$ docker pull celery@sha256:913d240525291580bee19f45e52e0e534b549567d4af73612e0e6d22160f7e20
```

-	Platforms:
	-	linux; amd64

### `celery:3` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81750893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144dc6bd2859dff3952a2310aaed138a6bd245f9a108fcd0ea5061bafe697122`
-	Default Command: `["celery","worker"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 20:40:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 20:40:14 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 22:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:31:10 GMT
ENV GPG_KEY=97FC712E4C024BBEA48A61ED3A5CA953F73C700D
# Tue, 28 Feb 2017 22:36:58 GMT
ENV PYTHON_VERSION=3.5.3
# Tue, 28 Feb 2017 22:36:58 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 28 Feb 2017 22:38:48 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libgdbm-dev 		liblzma-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-loadable-sqlite-extensions 		--enable-shared 	&& make -j$(nproc) 	&& make install 	&& ldconfig 		&& if [ ! -e /usr/local/bin/pip3 ]; then : 		&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python3 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	; fi 	&& pip3 install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 28 Feb 2017 22:38:49 GMT
RUN cd /usr/local/bin 	&& { [ -e easy_install ] || ln -s easy_install-* easy_install; } 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 28 Feb 2017 22:38:49 GMT
CMD ["python3"]
# Wed, 01 Mar 2017 01:45:11 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Wed, 01 Mar 2017 01:45:11 GMT
WORKDIR /home/user
# Wed, 01 Mar 2017 01:45:16 GMT
RUN pip install redis
# Wed, 01 Mar 2017 01:45:16 GMT
ENV CELERY_VERSION=3.1.25
# Wed, 01 Mar 2017 01:45:22 GMT
RUN pip install celery=="$CELERY_VERSION"
# Wed, 01 Mar 2017 01:45:23 GMT
RUN { 	echo 'import os'; 	echo "BROKER_URL = os.environ.get('CELERY_BROKER_URL', 'amqp://')"; } > celeryconfig.py
# Wed, 01 Mar 2017 01:45:23 GMT
ENV CELERY_BROKER_URL=amqp://guest@rabbit
# Wed, 01 Mar 2017 01:45:23 GMT
USER [user]
# Wed, 01 Mar 2017 01:45:24 GMT
CMD ["celery" "worker"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764f950e58321d40da999d0b1da856017c3b0faecaf1f6b02c228b7c854ac450`  
		Last Modified: Wed, 01 Mar 2017 15:55:20 GMT  
		Size: 3.3 MB (3344487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7929bfadb7abb12cab2fbe98cecd4bf9e76ac1798a91ae0724306ef92382b19f`  
		Last Modified: Wed, 01 Mar 2017 16:08:02 GMT  
		Size: 21.0 MB (20951735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8b59f20dbc72d93c9922c6ebd4e951d9bf553ea7174b47a3ffab15c5410228`  
		Last Modified: Wed, 01 Mar 2017 16:07:50 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3da70a026a508593be13faa499639ffe0f9cf32461d38bf1f758f11abf3e9c`  
		Last Modified: Wed, 01 Mar 2017 22:52:15 GMT  
		Size: 4.3 KB (4346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e0e7f8761108192c0298a9a8250b85523d27d2148f01aa26a080b2c8e9ee74`  
		Last Modified: Wed, 01 Mar 2017 22:52:17 GMT  
		Size: 1.8 MB (1849021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123afa2ec3b970bb05181661689a6d99edf03a4cd1acba5fa4791195c3e8840e`  
		Last Modified: Wed, 01 Mar 2017 22:52:18 GMT  
		Size: 4.2 MB (4237430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa0d7142d0e0f8954aee117b21ba3778ed12c9c4b8813a5f80e01ab9140e030`  
		Last Modified: Wed, 01 Mar 2017 22:52:16 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `celery:latest`

```console
$ docker pull celery@sha256:913d240525291580bee19f45e52e0e534b549567d4af73612e0e6d22160f7e20
```

-	Platforms:
	-	linux; amd64

### `celery:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81750893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144dc6bd2859dff3952a2310aaed138a6bd245f9a108fcd0ea5061bafe697122`
-	Default Command: `["celery","worker"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 20:40:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 20:40:14 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 22:15:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libgdbm3 		libsqlite3-0 		libssl1.0.0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:31:10 GMT
ENV GPG_KEY=97FC712E4C024BBEA48A61ED3A5CA953F73C700D
# Tue, 28 Feb 2017 22:36:58 GMT
ENV PYTHON_VERSION=3.5.3
# Tue, 28 Feb 2017 22:36:58 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Tue, 28 Feb 2017 22:38:48 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		libbz2-dev 		libc6-dev 		libgdbm-dev 		liblzma-dev 		libncurses-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tcl-dev 		tk-dev 		wget 		xz-utils 		zlib1g-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& rm -r "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& ./configure 		--enable-loadable-sqlite-extensions 		--enable-shared 	&& make -j$(nproc) 	&& make install 	&& ldconfig 		&& if [ ! -e /usr/local/bin/pip3 ]; then : 		&& wget -O /tmp/get-pip.py 'https://bootstrap.pypa.io/get-pip.py' 		&& python3 /tmp/get-pip.py "pip==$PYTHON_PIP_VERSION" 		&& rm /tmp/get-pip.py 	; fi 	&& pip3 install --no-cache-dir --upgrade --force-reinstall "pip==$PYTHON_PIP_VERSION" 	&& [ "$(pip list |tac|tac| awk -F '[ ()]+' '$1 == "pip" { print $2; exit }')" = "$PYTHON_PIP_VERSION" ] 		&& find /usr/local -depth 		\( 			\( -type d -a -name test -o -name tests \) 			-o 			\( -type f -a -name '*.pyc' -o -name '*.pyo' \) 		\) -exec rm -rf '{}' + 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/python ~/.cache
# Tue, 28 Feb 2017 22:38:49 GMT
RUN cd /usr/local/bin 	&& { [ -e easy_install ] || ln -s easy_install-* easy_install; } 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Tue, 28 Feb 2017 22:38:49 GMT
CMD ["python3"]
# Wed, 01 Mar 2017 01:45:11 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Wed, 01 Mar 2017 01:45:11 GMT
WORKDIR /home/user
# Wed, 01 Mar 2017 01:45:16 GMT
RUN pip install redis
# Wed, 01 Mar 2017 01:45:16 GMT
ENV CELERY_VERSION=3.1.25
# Wed, 01 Mar 2017 01:45:22 GMT
RUN pip install celery=="$CELERY_VERSION"
# Wed, 01 Mar 2017 01:45:23 GMT
RUN { 	echo 'import os'; 	echo "BROKER_URL = os.environ.get('CELERY_BROKER_URL', 'amqp://')"; } > celeryconfig.py
# Wed, 01 Mar 2017 01:45:23 GMT
ENV CELERY_BROKER_URL=amqp://guest@rabbit
# Wed, 01 Mar 2017 01:45:23 GMT
USER [user]
# Wed, 01 Mar 2017 01:45:24 GMT
CMD ["celery" "worker"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764f950e58321d40da999d0b1da856017c3b0faecaf1f6b02c228b7c854ac450`  
		Last Modified: Wed, 01 Mar 2017 15:55:20 GMT  
		Size: 3.3 MB (3344487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7929bfadb7abb12cab2fbe98cecd4bf9e76ac1798a91ae0724306ef92382b19f`  
		Last Modified: Wed, 01 Mar 2017 16:08:02 GMT  
		Size: 21.0 MB (20951735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8b59f20dbc72d93c9922c6ebd4e951d9bf553ea7174b47a3ffab15c5410228`  
		Last Modified: Wed, 01 Mar 2017 16:07:50 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3da70a026a508593be13faa499639ffe0f9cf32461d38bf1f758f11abf3e9c`  
		Last Modified: Wed, 01 Mar 2017 22:52:15 GMT  
		Size: 4.3 KB (4346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e0e7f8761108192c0298a9a8250b85523d27d2148f01aa26a080b2c8e9ee74`  
		Last Modified: Wed, 01 Mar 2017 22:52:17 GMT  
		Size: 1.8 MB (1849021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123afa2ec3b970bb05181661689a6d99edf03a4cd1acba5fa4791195c3e8840e`  
		Last Modified: Wed, 01 Mar 2017 22:52:18 GMT  
		Size: 4.2 MB (4237430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa0d7142d0e0f8954aee117b21ba3778ed12c9c4b8813a5f80e01ab9140e030`  
		Last Modified: Wed, 01 Mar 2017 22:52:16 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
