## `postgres:latest`

```console
$ docker pull postgres@sha256:6ac0fbeddde3bb7b0003a2ace8c126f742f8bdd90695801337d3edaaf1fcc478
```

-	Platforms:
	-	linux; amd64

### `postgres:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101800123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e18b2c30f8d0c8957f51f147feeeb631109e5dbc8476311a73603f48988f7eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 18:09:54 GMT
RUN groupadd -r postgres --gid=999 && useradd -r -g postgres --uid=999 postgres
# Tue, 28 Feb 2017 18:09:55 GMT
ENV GOSU_VERSION=1.7
# Tue, 28 Feb 2017 20:35:41 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 28 Feb 2017 20:35:50 GMT
RUN apt-get update && apt-get install -y locales && rm -rf /var/lib/apt/lists/* 	&& localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 28 Feb 2017 20:35:50 GMT
ENV LANG=en_US.utf8
# Tue, 28 Feb 2017 20:35:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Feb 2017 20:35:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 28 Feb 2017 20:35:53 GMT
ENV PG_MAJOR=9.6
# Tue, 28 Feb 2017 20:35:53 GMT
ENV PG_VERSION=9.6.2-1.pgdg80+1
# Tue, 28 Feb 2017 20:35:54 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jessie-pgdg main' $PG_MAJOR > /etc/apt/sources.list.d/pgdg.list
# Tue, 28 Feb 2017 20:36:28 GMT
RUN apt-get update 	&& apt-get install -y postgresql-common 	&& sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf 	&& apt-get install -y 		postgresql-$PG_MAJOR=$PG_VERSION 		postgresql-contrib-$PG_MAJOR=$PG_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 20:36:29 GMT
RUN mv -v /usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample /usr/share/postgresql/ 	&& ln -sv ../postgresql.conf.sample /usr/share/postgresql/$PG_MAJOR/ 	&& sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample
# Tue, 28 Feb 2017 20:36:30 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod g+s /var/run/postgresql
# Tue, 28 Feb 2017 20:36:30 GMT
ENV PATH=/usr/lib/postgresql/9.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 20:36:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 28 Feb 2017 20:36:31 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA" # this 777 will be replaced by 700 at runtime (allows semi-arbitrary "--user" values)
# Tue, 28 Feb 2017 20:36:32 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 28 Feb 2017 20:36:32 GMT
COPY file:8d267d76d9551f01f3b15b68c484da091c34fd675a9b6adc8c279d52364efdfc in /usr/local/bin/ 
# Tue, 28 Feb 2017 20:36:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 28 Feb 2017 20:36:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Feb 2017 20:36:34 GMT
EXPOSE 5432/tcp
# Tue, 28 Feb 2017 20:36:34 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b3eb81653480d6e9cd3e08d0f9bde54ee10a2ebb39def924b15f4c6f3ee259`  
		Last Modified: Thu, 02 Mar 2017 03:16:16 GMT  
		Size: 2.0 KB (2042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8428acbbc47ce0256cb935c2a00e1f94c56fddd0fd4e7cf94f120bfa063ad6a7`  
		Last Modified: Thu, 02 Mar 2017 03:16:16 GMT  
		Size: 1.2 MB (1216875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19552fac5eff8e5c7247c4554ea60b4c6376c2787563935b524dc1eba99c38e0`  
		Last Modified: Thu, 02 Mar 2017 03:16:17 GMT  
		Size: 6.9 MB (6865989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f19eddaec7204bf930c93ace1f31e9d5c89f5cbc60a6550668e549bd4d9304c`  
		Last Modified: Thu, 02 Mar 2017 03:16:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b476232c64c2168aeb466380eeccf32925d30ecbe98d1011aead0b2ea9401fbd`  
		Last Modified: Thu, 02 Mar 2017 03:16:13 GMT  
		Size: 4.5 KB (4484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e964c853634f77b63f7d3ab423e7e5b9e429a6a077284a25e14c6c5625833d57`  
		Last Modified: Thu, 02 Mar 2017 03:20:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1868280d339f98e03a56ee158f04873a4a7685b8dd76cded639945911e392e58`  
		Last Modified: Thu, 02 Mar 2017 03:20:18 GMT  
		Size: 42.3 MB (42337788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71b256a9a26e5bf5a4f9c00baab7ac4dc7fe107d068fb05e57ffc162851546b`  
		Last Modified: Thu, 02 Mar 2017 03:20:01 GMT  
		Size: 7.1 KB (7124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c0a0e9a89a751c45e10b239fb627fad878c918f6842fbaa058ddf889b7b287`  
		Last Modified: Thu, 02 Mar 2017 03:20:01 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8a526087193d31f07584b6a7f6211a4809a3772f8735ecbae9d2094d6ba21e`  
		Last Modified: Thu, 02 Mar 2017 03:20:01 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baead22f2b069d31386b501316aeb08fc8cf2a88f68f78071e05ddd3799d8f12`  
		Last Modified: Thu, 02 Mar 2017 03:20:00 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6deeab32da54c31327a8788c367357564be3906ff5af2515aa55c14c2f51e8`  
		Last Modified: Thu, 02 Mar 2017 03:20:01 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
