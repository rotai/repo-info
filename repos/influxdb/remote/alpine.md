## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:3e3c12aa740a3c0ba00843591360274b9750886a1b11721381b9f278562454d9
```

-	Platforms:
	-	linux; amd64

### `influxdb:alpine` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14139756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33dbd610be0a85b52a36f9320819c9bb3bd81f96b0a773bef55a15e33006118d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:37 GMT
ADD file:730030a984f5f0c5dc9b15ab61da161082b5c0f6e112a9c921b42321140c3927 in / 
# Wed, 08 Mar 2017 22:37:05 GMT
ENV INFLUXDB_VERSION=1.2.1
# Wed, 08 Mar 2017 22:37:27 GMT
RUN apk add --no-cache --virtual .build-deps wget gnupg tar ca-certificates &&     update-ca-certificates &&     gpg --keyserver hkp://ha.pool.sks-keyservers.net         --recv-keys 05CE15085FC09D18E99EFB22684A14CF2582E0C5 &&     wget -q https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget -q https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 08 Mar 2017 22:37:28 GMT
COPY file:3ee2bc0321c2aa2451df7a508649c3a54f0eebc1ef9b8a24967c58105b4d3160 in /etc/influxdb/influxdb.conf 
# Wed, 08 Mar 2017 22:37:28 GMT
EXPOSE 8086/tcp
# Wed, 08 Mar 2017 22:37:28 GMT
VOLUME [/var/lib/influxdb]
# Wed, 08 Mar 2017 22:37:29 GMT
COPY file:69ba622c5d14acee69909e208de64bf13aa81f0010ff82238c8825ba99d65290 in /entrypoint.sh 
# Wed, 08 Mar 2017 22:37:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Mar 2017 22:37:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:627beaf3eaaff1c0bc3311d60fb933c17ad04fe377e1043d9593646d8ae3bfe1`  
		Last Modified: Fri, 03 Mar 2017 20:34:41 GMT  
		Size: 1.9 MB (1905270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a789ac57e045b87fed0c8c31603152d6cfcc4839332c902b493c51532a1860e6`  
		Last Modified: Wed, 08 Mar 2017 22:40:13 GMT  
		Size: 12.2 MB (12234082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0487cbb471ca509a4e6738d706f284a9bbbd5eefa646f4c9762a09c101fb8bc7`  
		Last Modified: Wed, 08 Mar 2017 22:40:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473ba2e7bb1542bccb2d81f1153a28e3e02aac2ce1a5e68bed551c8ead3c41aa`  
		Last Modified: Wed, 08 Mar 2017 22:40:09 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
