<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `thrift`

-	[`thrift:0.9`](#thrift09)
-	[`thrift:0.9.3`](#thrift093)
-	[`thrift:0.10`](#thrift010)
-	[`thrift:0.10.0`](#thrift0100)
-	[`thrift:latest`](#thriftlatest)

## `thrift:0.9`

```console
$ docker pull thrift@sha256:36625bacea7e6100375780fb6901612dd6a60820a62e10c1e0ef37093b55b6ae
```

-	Platforms:
	-	linux; amd64

### `thrift:0.9` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49230988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c887a38693b09a8cd9d357c2e52e1a8362e21d427cdc33756dd8fb19cf84d5f1`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 27 Feb 2017 20:39:24 GMT
ADD file:ddbcd17149470ca923569d3112a7955f842a00bf8eee92781c6eb13af64b5b82 in / 
# Mon, 27 Feb 2017 20:39:25 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 00:50:41 GMT
MAINTAINER Adam Hawkins <adam@hawkins.io>
# Tue, 28 Feb 2017 00:50:42 GMT
ENV THRIFT_VERSION=0.9.3
# Tue, 28 Feb 2017 00:54:26 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Tue, 28 Feb 2017 00:54:27 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:c3e97b7a4c20461eb05807e795f449cc8826084be5e3c4766fa9cc49b4df3551`  
		Last Modified: Mon, 27 Feb 2017 20:50:15 GMT  
		Size: 37.3 MB (37284709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264fef4d374d22e5f4be3c52dd2f384a6f229120f278343b90f0cdff1ff1a8e6`  
		Last Modified: Tue, 28 Feb 2017 00:58:28 GMT  
		Size: 11.9 MB (11946279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `thrift:0.9.3`

```console
$ docker pull thrift@sha256:36625bacea7e6100375780fb6901612dd6a60820a62e10c1e0ef37093b55b6ae
```

-	Platforms:
	-	linux; amd64

### `thrift:0.9.3` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49230988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c887a38693b09a8cd9d357c2e52e1a8362e21d427cdc33756dd8fb19cf84d5f1`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 27 Feb 2017 20:39:24 GMT
ADD file:ddbcd17149470ca923569d3112a7955f842a00bf8eee92781c6eb13af64b5b82 in / 
# Mon, 27 Feb 2017 20:39:25 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 00:50:41 GMT
MAINTAINER Adam Hawkins <adam@hawkins.io>
# Tue, 28 Feb 2017 00:50:42 GMT
ENV THRIFT_VERSION=0.9.3
# Tue, 28 Feb 2017 00:54:26 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Tue, 28 Feb 2017 00:54:27 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:c3e97b7a4c20461eb05807e795f449cc8826084be5e3c4766fa9cc49b4df3551`  
		Last Modified: Mon, 27 Feb 2017 20:50:15 GMT  
		Size: 37.3 MB (37284709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264fef4d374d22e5f4be3c52dd2f384a6f229120f278343b90f0cdff1ff1a8e6`  
		Last Modified: Tue, 28 Feb 2017 00:58:28 GMT  
		Size: 11.9 MB (11946279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `thrift:0.10`

```console
$ docker pull thrift@sha256:50183b89fe94b14754c6c0f148970162e25a9645b0fefd4c4a3bdc1bfc2148f6
```

-	Platforms:
	-	linux; amd64

### `thrift:0.10` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50266288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5145f5801387a493fd30633219dd0e463073379a7c9651335af18cb298e317`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 27 Feb 2017 20:39:24 GMT
ADD file:ddbcd17149470ca923569d3112a7955f842a00bf8eee92781c6eb13af64b5b82 in / 
# Mon, 27 Feb 2017 20:39:25 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 00:54:27 GMT
MAINTAINER Adam Hawkins <hi@ahawkins.me>
# Tue, 28 Feb 2017 00:54:28 GMT
ENV THRIFT_VERSION=0.10.0
# Tue, 28 Feb 2017 00:57:53 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Tue, 28 Feb 2017 00:57:54 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:c3e97b7a4c20461eb05807e795f449cc8826084be5e3c4766fa9cc49b4df3551`  
		Last Modified: Mon, 27 Feb 2017 20:50:15 GMT  
		Size: 37.3 MB (37284709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2810efde993c5ee2ae659963d412637b4dd919e10ca07c5bc4f7fafff9072e0`  
		Last Modified: Tue, 28 Feb 2017 00:59:19 GMT  
		Size: 13.0 MB (12981579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `thrift:0.10.0`

```console
$ docker pull thrift@sha256:50183b89fe94b14754c6c0f148970162e25a9645b0fefd4c4a3bdc1bfc2148f6
```

-	Platforms:
	-	linux; amd64

### `thrift:0.10.0` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50266288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5145f5801387a493fd30633219dd0e463073379a7c9651335af18cb298e317`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 27 Feb 2017 20:39:24 GMT
ADD file:ddbcd17149470ca923569d3112a7955f842a00bf8eee92781c6eb13af64b5b82 in / 
# Mon, 27 Feb 2017 20:39:25 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 00:54:27 GMT
MAINTAINER Adam Hawkins <hi@ahawkins.me>
# Tue, 28 Feb 2017 00:54:28 GMT
ENV THRIFT_VERSION=0.10.0
# Tue, 28 Feb 2017 00:57:53 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Tue, 28 Feb 2017 00:57:54 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:c3e97b7a4c20461eb05807e795f449cc8826084be5e3c4766fa9cc49b4df3551`  
		Last Modified: Mon, 27 Feb 2017 20:50:15 GMT  
		Size: 37.3 MB (37284709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2810efde993c5ee2ae659963d412637b4dd919e10ca07c5bc4f7fafff9072e0`  
		Last Modified: Tue, 28 Feb 2017 00:59:19 GMT  
		Size: 13.0 MB (12981579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `thrift:latest`

```console
$ docker pull thrift@sha256:50183b89fe94b14754c6c0f148970162e25a9645b0fefd4c4a3bdc1bfc2148f6
```

-	Platforms:
	-	linux; amd64

### `thrift:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50266288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5145f5801387a493fd30633219dd0e463073379a7c9651335af18cb298e317`
-	Default Command: `["thrift"]`

```dockerfile
# Mon, 27 Feb 2017 20:39:24 GMT
ADD file:ddbcd17149470ca923569d3112a7955f842a00bf8eee92781c6eb13af64b5b82 in / 
# Mon, 27 Feb 2017 20:39:25 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 00:54:27 GMT
MAINTAINER Adam Hawkins <hi@ahawkins.me>
# Tue, 28 Feb 2017 00:54:28 GMT
ENV THRIFT_VERSION=0.10.0
# Tue, 28 Feb 2017 00:57:53 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Tue, 28 Feb 2017 00:57:54 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:c3e97b7a4c20461eb05807e795f449cc8826084be5e3c4766fa9cc49b4df3551`  
		Last Modified: Mon, 27 Feb 2017 20:50:15 GMT  
		Size: 37.3 MB (37284709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2810efde993c5ee2ae659963d412637b4dd919e10ca07c5bc4f7fafff9072e0`  
		Last Modified: Tue, 28 Feb 2017 00:59:19 GMT  
		Size: 13.0 MB (12981579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
