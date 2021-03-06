## `jetty:jre7`

```console
$ docker pull jetty@sha256:1e8edb4dd55456e9b99f74b382c21934e9338cf414bbd57e0b65f04219a10cee
```

-	Platforms:
	-	linux; amd64

### `jetty:jre7` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158302871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b845a19f8028259e0356fc7dbd7782da283a27a7f08930b7adccbd6183cc158b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 15:23:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 15:23:25 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 15:23:26 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 28 Feb 2017 15:23:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-7-openjdk-amd64/jre
# Tue, 28 Feb 2017 15:23:27 GMT
ENV JAVA_VERSION=7u121
# Tue, 28 Feb 2017 15:23:27 GMT
ENV JAVA_DEBIAN_VERSION=7u121-2.6.8-2~deb8u1
# Tue, 28 Feb 2017 15:24:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		openjdk-7-jre-headless="$JAVA_DEBIAN_VERSION" 	&& rm -rf /var/lib/apt/lists/* 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 01 Mar 2017 15:41:57 GMT
RUN groupadd -r jetty && useradd -r -g jetty jetty
# Wed, 01 Mar 2017 15:41:57 GMT
ENV JETTY_HOME=/usr/local/jetty
# Wed, 01 Mar 2017 15:41:58 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2017 15:41:58 GMT
RUN mkdir -p "$JETTY_HOME"
# Wed, 01 Mar 2017 15:41:59 GMT
WORKDIR /usr/local/jetty
# Wed, 01 Mar 2017 15:41:59 GMT
ENV JETTY_VERSION=9.2.21.v20170120
# Wed, 01 Mar 2017 15:41:59 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.2.21.v20170120/jetty-distribution-9.2.21.v20170120.tar.gz
# Wed, 01 Mar 2017 15:42:00 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D
# Wed, 01 Mar 2017 15:42:04 GMT
RUN set -xe 	&& curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz 	&& curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in $JETTY_GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; done 	&& gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz 	&& rm -r "$GNUPGHOME" 	&& tar -xvf jetty.tar.gz --strip-components=1 	&& sed -i '/jetty-logging/d' etc/jetty.conf 	&& rm -fr demo-base javadoc 	&& rm jetty.tar.gz* 	&& rm -rf /tmp/hsperfdata_root
# Wed, 01 Mar 2017 15:42:04 GMT
ENV JETTY_BASE=/var/lib/jetty
# Wed, 01 Mar 2017 15:42:05 GMT
RUN mkdir -p "$JETTY_BASE"
# Wed, 01 Mar 2017 15:42:05 GMT
WORKDIR /var/lib/jetty
# Wed, 01 Mar 2017 15:42:09 GMT
RUN modules="$(grep -- ^--module= "$JETTY_HOME/start.ini" | cut -d= -f2 | paste -d, -s)" 	&& set -xe 	&& java -jar "$JETTY_HOME/start.jar" --add-to-startd="$modules,setuid" 	&& chown -R jetty:jetty "$JETTY_BASE" 	&& rm -rf /tmp/hsperfdata_root
# Wed, 01 Mar 2017 15:42:09 GMT
ENV TMPDIR=/tmp/jetty
# Wed, 01 Mar 2017 15:42:10 GMT
RUN set -xe 	&& mkdir -p "$TMPDIR" 	&& chown -R jetty:jetty "$TMPDIR"
# Wed, 01 Mar 2017 15:42:10 GMT
COPY file:4f7da2906a90932cfb90db54a45ee08f86b17253747db62085f7512c9efd46ad in / 
# Wed, 01 Mar 2017 15:42:11 GMT
EXPOSE 8080/tcp
# Wed, 01 Mar 2017 15:42:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Mar 2017 15:42:11 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081cd4bfd5210ff69949cc356db9693d11d103cd2380117cff7d4be6966eafdf`  
		Last Modified: Mon, 27 Feb 2017 21:53:23 GMT  
		Size: 18.5 MB (18535995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8d00ed730f283f3b242d69afa12b3b654475f2de8cbb137f972f2645e076bf`  
		Last Modified: Tue, 28 Feb 2017 21:56:45 GMT  
		Size: 566.8 KB (566834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fd21b2210400e7764782a10451f499b6df86fae6ba5724557871c4b24621ca`  
		Last Modified: Tue, 28 Feb 2017 21:56:47 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67cd8115494e7b08a6478d778d1981e74ddd5eaf074e85e91d748ad3b577f85`  
		Last Modified: Tue, 28 Feb 2017 21:57:07 GMT  
		Size: 77.8 MB (77812863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93470aea9ecb8b515316f727594fec170cc43d5cc58366daed902af935991f0`  
		Last Modified: Thu, 02 Mar 2017 05:36:50 GMT  
		Size: 2.1 KB (2083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0370a0418efebc09a51c78a282ce58834490bc70b57d0d0ae31a731fcd4ac5f`  
		Last Modified: Thu, 02 Mar 2017 05:36:50 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1cd2335e91eb944f53087cecb9d0884674b8e027c181dfb9b6aab0fd44d689`  
		Last Modified: Thu, 02 Mar 2017 05:36:49 GMT  
		Size: 10.0 MB (10018956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9109de10f1b0344c35905c6103332febc171b46c82ea6e4ee419a05bc1c030`  
		Last Modified: Thu, 02 Mar 2017 05:36:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f0de9141553f58634950daffba408b23881f3bc78ef0f7ee2210d66159890d`  
		Last Modified: Thu, 02 Mar 2017 05:36:47 GMT  
		Size: 1.6 KB (1551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abff2adc6af83dafeda2ce3144ec4025b8b4b90a452a11f732113580d032f19`  
		Last Modified: Thu, 02 Mar 2017 05:36:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec4649cb985c7baba6143faea8cdd0ba3250c20b5d4ef35a93e94e3398f320a`  
		Last Modified: Thu, 02 Mar 2017 05:36:42 GMT  
		Size: 572.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
