## `sonarqube:alpine`

```console
$ docker pull sonarqube@sha256:afa1cf1b5a39681059a3ec214658498e2f44e13194816e36ce16c988804bc243
```

-	Platforms:
	-	linux; amd64

### `sonarqube:alpine` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (186006629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dc768c7398415b20703aef1bb86ff107141ab17e7a475a5589c259e9c602cd`
-	Entrypoint: `[".\/bin\/run.sh"]`

```dockerfile
# Fri, 03 Mar 2017 20:32:21 GMT
ADD file:3df55c321c1c8d73f22bc69240c0764290d6cb293da46ba8f94ed25473fb5853 in / 
# Fri, 03 Mar 2017 22:00:57 GMT
ENV LANG=C.UTF-8
# Fri, 03 Mar 2017 22:00:58 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 03 Mar 2017 22:01:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk
# Fri, 03 Mar 2017 22:01:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Fri, 03 Mar 2017 22:01:21 GMT
ENV JAVA_VERSION=8u111
# Fri, 03 Mar 2017 22:01:22 GMT
ENV JAVA_ALPINE_VERSION=8.111.14-r0
# Fri, 03 Mar 2017 22:01:26 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Fri, 03 Mar 2017 23:44:33 GMT
MAINTAINER David Gageot <david.gageot@sonarsource.com>
# Fri, 03 Mar 2017 23:44:51 GMT
ENV SONAR_VERSION=6.2 SONARQUBE_HOME=/opt/sonarqube SONARQUBE_JDBC_USERNAME=sonar SONARQUBE_JDBC_PASSWORD=sonar SONARQUBE_JDBC_URL=
# Fri, 03 Mar 2017 23:44:51 GMT
EXPOSE 9000/tcp
# Fri, 03 Mar 2017 23:45:02 GMT
RUN set -x     && apk add --no-cache gnupg unzip curl     && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys F1182E81C792928921DBCAB4CFCA4A29D26468DE     && mkdir /opt     && cd /opt     && curl -o sonarqube.zip -fSL https://sonarsource.bintray.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip     && curl -o sonarqube.zip.asc -fSL https://sonarsource.bintray.com/Distribution/sonarqube/sonarqube-$SONAR_VERSION.zip.asc     && gpg --batch --verify sonarqube.zip.asc sonarqube.zip     && unzip sonarqube.zip     && mv sonarqube-$SONAR_VERSION sonarqube     && rm sonarqube.zip*     && rm -rf $SONARQUBE_HOME/bin/*
# Fri, 03 Mar 2017 23:45:03 GMT
VOLUME [/opt/sonarqube/data]
# Fri, 03 Mar 2017 23:45:03 GMT
WORKDIR /opt/sonarqube
# Fri, 03 Mar 2017 23:45:04 GMT
COPY file:83e169627dc34c4308fd222d47a1ae7c388a283efdc49980a885a8788308a052 in /opt/sonarqube/bin/ 
# Fri, 03 Mar 2017 23:45:04 GMT
ENTRYPOINT ["./bin/run.sh"]
```

-	Layers:
	-	`sha256:7095154754192bfc2306f3b2b841ef82771b7ad39526537234adb1e74ae81a93`  
		Last Modified: Fri, 03 Mar 2017 20:34:19 GMT  
		Size: 2.3 MB (2313384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a1c0aaa6fda9a4f5f940c5c7a0622430f1faac9de367016cd5a0aed8ef4478`  
		Last Modified: Sat, 04 Mar 2017 01:28:19 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b58c996e33ea9b6701cb8935434be70cb9e5908d81a81f360b47e6f9394a1d7`  
		Last Modified: Sat, 04 Mar 2017 02:56:01 GMT  
		Size: 49.4 MB (49360641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5366d0a0895318ad2e39a5729c11034621b50c3158bdce7a0552f2c834455b6d`  
		Last Modified: Sat, 04 Mar 2017 06:05:01 GMT  
		Size: 134.3 MB (134331943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648001a8737a7b57bddd3bf4cca6c4da4ee5b232de2e27f10d02c991ee380788`  
		Last Modified: Sat, 04 Mar 2017 06:04:22 GMT  
		Size: 433.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
