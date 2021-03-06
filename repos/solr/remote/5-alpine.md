## `solr:5-alpine`

```console
$ docker pull solr@sha256:e8b2291a49ac5c874f624e9e6f3a221bb7f74260d7f8f1974e19763163c0c274
```

-	Platforms:
	-	linux; amd64

### `solr:5-alpine` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193353917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b34fb41d4b31a1415e7df18d9b78fb5da1207989cc45911b2ba2192c10872be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:37 GMT
ADD file:730030a984f5f0c5dc9b15ab61da161082b5c0f6e112a9c921b42321140c3927 in / 
# Tue, 07 Mar 2017 01:03:58 GMT
ENV LANG=C.UTF-8
# Tue, 07 Mar 2017 01:03:59 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 07 Mar 2017 01:04:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk/jre
# Tue, 07 Mar 2017 01:04:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Tue, 07 Mar 2017 01:04:10 GMT
ENV JAVA_VERSION=8u121
# Tue, 07 Mar 2017 01:04:10 GMT
ENV JAVA_ALPINE_VERSION=8.121.13-r0
# Tue, 07 Mar 2017 01:04:15 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8-jre="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Tue, 07 Mar 2017 20:02:13 GMT
MAINTAINER Martijn Koster "mak-docker@greenhills.co.uk"
# Tue, 07 Mar 2017 20:02:13 GMT
ARG SOLR_DOWNLOAD_SERVER
# Tue, 07 Mar 2017 20:02:14 GMT
ARG GPG_KEYSERVER
# Tue, 07 Mar 2017 20:02:18 GMT
RUN apk add --no-cache         lsof         gnupg         procps         tar         bash
# Tue, 07 Mar 2017 20:02:20 GMT
RUN apk add --no-cache ca-certificates wget &&         update-ca-certificates
# Tue, 07 Mar 2017 20:02:21 GMT
ENV SOLR_USER=solr
# Tue, 07 Mar 2017 20:02:22 GMT
ENV SOLR_UID=8983
# Tue, 07 Mar 2017 20:02:23 GMT
RUN addgroup -S -g $SOLR_UID $SOLR_USER &&   adduser -S -u $SOLR_UID -g $SOLR_USER $SOLR_USER
# Tue, 07 Mar 2017 20:02:23 GMT
ENV SOLR_KEY=EDF961FF03E647F9CA8A9C2C758051CCA3A13A7F
# Tue, 07 Mar 2017 20:02:27 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$SOLR_KEY"
# Tue, 07 Mar 2017 20:02:28 GMT
ENV GPG_KEYSERVER=hkp://ha.pool.sks-keyservers.net
# Tue, 07 Mar 2017 20:02:31 GMT
RUN gpg --keyserver "$GPG_KEYSERVER" --recv-keys "$SOLR_KEY"
# Tue, 07 Mar 2017 20:02:31 GMT
ENV SOLR_VERSION=5.5.3
# Tue, 07 Mar 2017 20:02:32 GMT
ENV SOLR_SHA256=74e8a924dac0e073854af121a6de9d58fe8cc315d16b57e17f429c6a91b0b065
# Tue, 07 Mar 2017 20:02:33 GMT
ENV SOLR_URL=https://archive.apache.org/dist/lucene/solr/5.5.3/solr-5.5.3.tgz
# Tue, 07 Mar 2017 20:02:48 GMT
RUN mkdir -p /opt/solr &&   echo "downloading $SOLR_URL" &&   wget -q $SOLR_URL -O /opt/solr.tgz &&   echo "downloading $SOLR_URL.asc" &&   wget -q $SOLR_URL.asc -O /opt/solr.tgz.asc &&   echo "$SOLR_SHA256 */opt/solr.tgz" | sha256sum -c - &&   (>&2 ls -l /opt/solr.tgz /opt/solr.tgz.asc) &&   gpg --batch --verify /opt/solr.tgz.asc /opt/solr.tgz &&   tar -C /opt/solr --extract --file /opt/solr.tgz --strip-components=1 &&   rm /opt/solr.tgz* &&   rm -Rf /opt/solr/docs/ &&   mkdir -p /opt/solr/server/solr/lib /opt/solr/server/solr/mycores &&   sed -i -e 's/#SOLR_PORT=8983/SOLR_PORT=8983/' /opt/solr/bin/solr.in.sh &&   sed -i -e '/-Dsolr.clustering.enabled=true/ a SOLR_OPTS="$SOLR_OPTS -Dsun.net.inetaddr.ttl=60 -Dsun.net.inetaddr.negative.ttl=60"' /opt/solr/bin/solr.in.sh &&   chown -R $SOLR_USER:$SOLR_USER /opt/solr &&   mkdir /docker-entrypoint-initdb.d /opt/docker-solr/
# Tue, 07 Mar 2017 20:02:49 GMT
COPY dir:a1334d90f054a1dc82fff589ec6096bb7d4216f958abf3d6d6ce0238c93fa3b3 in /opt/docker-solr/scripts 
# Tue, 07 Mar 2017 20:02:51 GMT
RUN chown -R $SOLR_USER:$SOLR_USER /opt/docker-solr
# Tue, 07 Mar 2017 20:02:51 GMT
ENV PATH=/opt/solr/bin:/opt/docker-solr/scripts:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Tue, 07 Mar 2017 20:02:52 GMT
EXPOSE 8983/tcp
# Tue, 07 Mar 2017 20:02:52 GMT
WORKDIR /opt/solr
# Tue, 07 Mar 2017 20:02:53 GMT
USER [solr]
# Tue, 07 Mar 2017 20:02:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Mar 2017 20:02:54 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:627beaf3eaaff1c0bc3311d60fb933c17ad04fe377e1043d9593646d8ae3bfe1`  
		Last Modified: Fri, 03 Mar 2017 20:34:41 GMT  
		Size: 1.9 MB (1905270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de20f2d8b839756d5fc0ae6871096666a822b6b4205e11e9cf438a2263f3281`  
		Last Modified: Tue, 07 Mar 2017 01:12:49 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e619d348278f1e8660192734bff496a6c3e05aab6bef025e843e7413a7c9e3`  
		Last Modified: Tue, 07 Mar 2017 01:15:49 GMT  
		Size: 53.8 MB (53811092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecf8ac747ed36539dedfd7694f2bef0585857ac087b491e32d0cea148d73dcf`  
		Last Modified: Tue, 07 Mar 2017 20:05:21 GMT  
		Size: 5.2 MB (5165776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fbb7ff6d48b54e5e036c54aced5d919198efaad38ce770a27c568620b3c61a`  
		Last Modified: Tue, 07 Mar 2017 20:05:19 GMT  
		Size: 612.2 KB (612161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72286f66e6a4ef5326cb9718424abf5ab10ee9c87335cd55bb85ff05245866a1`  
		Last Modified: Tue, 07 Mar 2017 20:05:18 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aaf5149ecf81b196d48545345e7c8321dac1c52b7758409717241ec4b56aff7`  
		Last Modified: Tue, 07 Mar 2017 20:05:16 GMT  
		Size: 7.6 KB (7633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4e69fc939d1ba6e8bf73a03d0778977e81a8e7b58e8f7e0fc3174fc14ee2cf`  
		Last Modified: Tue, 07 Mar 2017 20:05:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98c7b89814ba4df13cbb1c229f42df809d49c6d5f24ec57223820a4c7e08707`  
		Last Modified: Tue, 07 Mar 2017 20:05:28 GMT  
		Size: 131.8 MB (131844408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf938c4535fc04008b398a57e7f9de3473fbc251cf9a21e62f3c0023bae5942d`  
		Last Modified: Tue, 07 Mar 2017 20:05:16 GMT  
		Size: 3.0 KB (2974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdee0211753433d27104f46d46b4c7faa4fd67bb7dda4e8f717a506f67a2cfc`  
		Last Modified: Tue, 07 Mar 2017 20:05:16 GMT  
		Size: 3.0 KB (2986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
