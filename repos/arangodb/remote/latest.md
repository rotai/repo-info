## `arangodb:latest`

```console
$ docker pull arangodb@sha256:ab8f1b85297cbda4e161f826a71674b6d64ebe4c2194f3868743e3bd9ca44218
```

-	Platforms:
	-	linux; amd64

### `arangodb:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127216417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:665c17ea4dfd667d5baf676253b8be4ba719f9105c2f50696f94e11ad2e3e950`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["arangod"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 22:40:58 GMT
MAINTAINER Frank Celler <info@arangodb.com>
# Mon, 27 Feb 2017 22:41:41 GMT
ENV ARCHITECTURE=amd64
# Mon, 27 Feb 2017 22:42:25 GMT
ENV DEB_PACKAGE_VERSION=1
# Tue, 07 Mar 2017 17:43:59 GMT
ENV ARANGO_VERSION=3.1.13
# Tue, 07 Mar 2017 17:44:00 GMT
ENV ARANGO_URL=https://www.arangodb.com/repositories/arangodb31/Debian_8.0
# Tue, 07 Mar 2017 17:44:00 GMT
ENV ARANGO_PACKAGE=arangodb3-3.1.13-1_amd64.deb
# Tue, 07 Mar 2017 17:44:01 GMT
ENV ARANGO_PACKAGE_URL=https://www.arangodb.com/repositories/arangodb31/Debian_8.0/amd64/arangodb3-3.1.13-1_amd64.deb
# Tue, 07 Mar 2017 17:44:01 GMT
ENV ARANGO_SIGNATURE_URL=https://www.arangodb.com/repositories/arangodb31/Debian_8.0/amd64/arangodb3-3.1.13-1_amd64.deb.asc
# Tue, 07 Mar 2017 17:44:18 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys CD8CB0F1E0AD5B52E93F41E7EA93F5E56E751E9B
# Tue, 07 Mar 2017 17:44:31 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libjemalloc1 	libsnappy1         ca-certificates         pwgen         curl     &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Mar 2017 17:44:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 07 Mar 2017 17:45:24 GMT
RUN curl -O ${ARANGO_SIGNATURE_URL} &&           curl -O ${ARANGO_PACKAGE_URL} &&             gpg --verify ${ARANGO_PACKAGE}.asc &&     (echo arangodb3 arangodb3/password password test | debconf-set-selections) &&     (echo arangodb3 arangodb3/password_again password test | debconf-set-selections) &&     DEBIAN_FRONTEND="noninteractive" dpkg -i ${ARANGO_PACKAGE} &&     rm -rf /var/lib/arangodb3/* &&     sed -ri         -e 's!127\.0\.0\.1!0.0.0.0!g'         -e 's!^(file\s*=).*!\1 -!'         -e 's!^#\s*uid\s*=.*!uid = arangodb!'         -e 's!^#\s*gid\s*=.*!gid = arangodb!'         /etc/arangodb3/arangod.conf     &&     DEBIAN_FRONTEND="noninteractive" apt-get purge -y --auto-remove ca-certificates &&     rm -f ${ARANGO_PACKAGE}*
# Tue, 07 Mar 2017 17:45:37 GMT
VOLUME [/var/lib/arangodb3 /var/lib/arangodb3-apps]
# Tue, 07 Mar 2017 17:45:38 GMT
COPY file:9f20ed9a2181af8ddc12371a0082e7645aa20b1008b5f484851bcc399e64801e in /entrypoint.sh 
# Tue, 07 Mar 2017 17:45:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Mar 2017 17:45:55 GMT
EXPOSE 8529/tcp
# Tue, 07 Mar 2017 17:45:56 GMT
CMD ["arangod"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0a64a721d9ba3bd9fe2014f10e8116e1d86cfbe851f7cb23522bc6f7707da`  
		Last Modified: Tue, 07 Mar 2017 17:46:53 GMT  
		Size: 7.4 KB (7369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88cf1b0f03432de460b6953fc781856bae93799ed80893f223208f45ca695f9`  
		Last Modified: Tue, 07 Mar 2017 17:46:55 GMT  
		Size: 6.7 MB (6691500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c551359a1328978cb9de2fc553e9d8c5d366ddbb3c8a7d105eebceacd80400ef`  
		Last Modified: Tue, 07 Mar 2017 17:46:53 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6a936db3db32ad42313a1de2750af836d305d3fe167033ff95f5155b339dc7`  
		Last Modified: Tue, 07 Mar 2017 17:47:14 GMT  
		Size: 69.2 MB (69152624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7054fc9d370d29610e53f212950957b389853c57f29dd6484950b7f35b3b0b`  
		Last Modified: Tue, 07 Mar 2017 17:46:53 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
