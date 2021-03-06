## `mongo:latest`

```console
$ docker pull mongo@sha256:3d4537f996bc28a6c6b694e22f46316c0629703420de60e8f46285ce1fe69260
```

-	Platforms:
	-	linux; amd64

### `mongo:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150420569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686238c7a975c9dcb154be65a2ea761b79e4401990860ab11549281e92f2e442`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 06:02:43 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Tue, 28 Feb 2017 06:02:48 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		numactl 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 06:02:49 GMT
ENV GOSU_VERSION=1.7
# Tue, 28 Feb 2017 06:03:31 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 28 Feb 2017 06:03:31 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Tue, 28 Feb 2017 06:03:33 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	rm -r "$GNUPGHOME"; 	apt-key list
# Tue, 28 Feb 2017 06:03:33 GMT
ENV MONGO_MAJOR=3.4
# Tue, 28 Feb 2017 06:03:33 GMT
ENV MONGO_VERSION=3.4.2
# Tue, 28 Feb 2017 06:03:34 GMT
ENV MONGO_PACKAGE=mongodb-org
# Tue, 28 Feb 2017 06:03:35 GMT
RUN echo "deb http://repo.mongodb.org/apt/debian jessie/mongodb-org/$MONGO_MAJOR main" > /etc/apt/sources.list.d/mongodb-org.list
# Tue, 28 Feb 2017 06:04:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 28 Feb 2017 06:04:42 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 28 Feb 2017 06:04:43 GMT
VOLUME [/data/db /data/configdb]
# Tue, 28 Feb 2017 06:04:44 GMT
COPY file:31c99192d9c1648c6f48dc5557de182c76080376f32685657130407fda705b3b in /entrypoint.sh 
# Tue, 28 Feb 2017 06:04:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Feb 2017 06:04:45 GMT
EXPOSE 27017/tcp
# Tue, 28 Feb 2017 06:04:45 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a29f630b22ecb9060e541038d275645574312de47421df2f8031621acb25d2f`  
		Last Modified: Thu, 02 Mar 2017 01:28:47 GMT  
		Size: 2.0 KB (2042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328ac2c79d69324cb76eb09114330606aaadbe073e6f6409e7cb131bcf287e5e`  
		Last Modified: Thu, 02 Mar 2017 01:28:47 GMT  
		Size: 134.4 KB (134448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d628f74e0e9702828e26ab68da68fefaf2fe69942556c90360c55c057b82fdc6`  
		Last Modified: Thu, 02 Mar 2017 01:28:47 GMT  
		Size: 1.2 MB (1217784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50753de132e0a3f79a598d92b47f33832a3915da40ff5636633b59e7c0b2e1f7`  
		Last Modified: Thu, 02 Mar 2017 01:29:48 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14fee098631ba283944156b1743f8eec8fb695c8e4fe2758fca9ef631badbff0`  
		Last Modified: Thu, 02 Mar 2017 01:29:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4c3bdc152539bddccffa8c1ac1f4aae8333eaecf265d539fe2cca0e4fb8b95`  
		Last Modified: Thu, 02 Mar 2017 01:30:19 GMT  
		Size: 97.7 MB (97700620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe0970b86ae43a0dbed0174ea6ff638ec1f8073308a14ceb2af0cc2c4a180da`  
		Last Modified: Thu, 02 Mar 2017 01:29:49 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fbca93d3445d1b12330b3ea1b965aa0fd80383d67a0ccd682c035f99c545b2`  
		Last Modified: Thu, 02 Mar 2017 01:29:48 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
