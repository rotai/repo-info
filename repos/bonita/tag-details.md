<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `bonita`

-	[`bonita:7.3.3`](#bonita733)
-	[`bonita:7.4.2`](#bonita742)
-	[`bonita:latest`](#bonitalatest)

## `bonita:7.3.3`

```console
$ docker pull bonita@sha256:5270db2c5bcc043ba25447bc6c7920359f5c2efb7a9bd8a0add83c34e777ba54
```

-	Platforms:
	-	linux; amd64

### `bonita:7.3.3` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216539747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c50df8dccf93e770c26d211328d51c3164ca1b1c3d820cef189d41b053f27c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 27 Feb 2017 19:40:39 GMT
ADD file:a642bdc2d8d6e4484e4419fc938e24b03454e36f389233f2ce77fc04722da900 in / 
# Mon, 27 Feb 2017 19:40:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 27 Feb 2017 19:40:49 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 19:41:05 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Mon, 27 Feb 2017 19:41:06 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 27 Feb 2017 19:41:06 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 22:43:09 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Mon, 27 Feb 2017 22:44:00 GMT
RUN apt-get update && apt-get install -y   mysql-client-core-5.5   openjdk-7-jre-headless   postgresql-client   unzip   wget   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 22:44:00 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 27 Feb 2017 22:44:01 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 27 Feb 2017 22:44:03 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4
# Mon, 27 Feb 2017 22:44:07 GMT
RUN wget -q "https://github.com/tianon/gosu/releases/download/1.6/gosu-$(dpkg --print-architecture)" -O /usr/local/bin/gosu   && wget -q "https://github.com/tianon/gosu/releases/download/1.6/gosu-$(dpkg --print-architecture).asc" -O /usr/local/bin/gosu.asc   && gpg --verify /usr/local/bin/gosu.asc   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 27 Feb 2017 22:44:08 GMT
ENV BONITA_VERSION=7.3.3
# Mon, 27 Feb 2017 22:44:08 GMT
ENV TOMCAT_VERSION=7.0.67
# Mon, 27 Feb 2017 22:44:08 GMT
ENV BONITA_SHA256=128911e3b6241e135b2dbc496d8ce383d921f2f2478fc5fad4331e1fd362eb4f
# Mon, 27 Feb 2017 22:44:09 GMT
ENV POSTGRES_JDBC_DRIVER=postgresql-9.3-1102.jdbc41.jar
# Mon, 27 Feb 2017 22:44:09 GMT
ENV POSTGRES_SHA256=b78749d536da75c382d0a71c717cde6850df64e16594676fc7cacb5a74541d66
# Mon, 27 Feb 2017 22:44:09 GMT
ENV MYSQL_JDBC_DRIVER=mysql-connector-java-5.1.26
# Mon, 27 Feb 2017 22:44:10 GMT
ENV MYSQL_SHA256=40b2d49f6f2551cc7fa54552af806e8026bf8405f03342205852e57a3205a868
# Mon, 27 Feb 2017 22:44:14 GMT
RUN mkdir /opt/files   && wget -q https://jdbc.postgresql.org/download/${POSTGRES_JDBC_DRIVER} -O /opt/files/${POSTGRES_JDBC_DRIVER}   && echo "$POSTGRES_SHA256" /opt/files/${POSTGRES_JDBC_DRIVER} | sha256sum -c -   && wget -q http://dev.mysql.com/get/Downloads/Connector-J/${MYSQL_JDBC_DRIVER}.zip -O /opt/files/${MYSQL_JDBC_DRIVER}.zip   && echo "$MYSQL_SHA256" /opt/files/${MYSQL_JDBC_DRIVER}.zip | sha256sum -c -   && unzip -q /opt/files/${MYSQL_JDBC_DRIVER}.zip -d /opt/files/   && mv /opt/files/${MYSQL_JDBC_DRIVER}/${MYSQL_JDBC_DRIVER}-bin.jar /opt/files/   && rm -r /opt/files/${MYSQL_JDBC_DRIVER}   && rm /opt/files/${MYSQL_JDBC_DRIVER}.zip
# Mon, 27 Feb 2017 22:44:25 GMT
RUN wget -q http://download.forge.ow2.org/bonita/BonitaBPMCommunity-${BONITA_VERSION}-Tomcat-${TOMCAT_VERSION}.zip -O /opt/files/BonitaBPMCommunity-${BONITA_VERSION}-Tomcat-${TOMCAT_VERSION}.zip   && echo "$BONITA_SHA256" /opt/files/BonitaBPMCommunity-${BONITA_VERSION}-Tomcat-${TOMCAT_VERSION}.zip | sha256sum -c -
# Mon, 27 Feb 2017 22:44:26 GMT
VOLUME [/opt/bonita]
# Mon, 27 Feb 2017 22:44:26 GMT
COPY dir:fde4873241031c6b90b44319c923aea3900e89716d18d78efb0f8fd43ac375a6 in /opt/files 
# Mon, 27 Feb 2017 22:44:27 GMT
COPY dir:02b08d3b2ed19a654c43e135e71e47c809262f2a015647ff3da638716f22696f in /opt/templates 
# Mon, 27 Feb 2017 22:44:27 GMT
EXPOSE 8080/tcp
# Mon, 27 Feb 2017 22:44:28 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:30d541b48fc05d2a1b2b0ac6a74f3df70e928c3edc253d5bce5dc6ae1fad55d2`  
		Last Modified: Mon, 27 Feb 2017 19:46:55 GMT  
		Size: 65.7 MB (65693630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecd7f80d390b9e9a009363abea9fb2bb53e8104b4fc2f7abe00ee254005af1c`  
		Last Modified: Mon, 27 Feb 2017 19:46:34 GMT  
		Size: 71.6 KB (71555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ec9927bb81d07ac2602292888b2c61213d51d1a4eeef6354fb9734246e52da`  
		Last Modified: Mon, 27 Feb 2017 19:46:34 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e67a4d67b44968a2e2b40b1a22c6ad3192a9a490f1a47824f1309f8b97d30e5`  
		Last Modified: Mon, 27 Feb 2017 19:46:34 GMT  
		Size: 680.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9dd91554882183cb5d1cd512479487e10f495c22d035a62fbb3ee38d89cf48`  
		Last Modified: Mon, 27 Feb 2017 19:46:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8a9ece2ab54505896ac4c64bf6c03753f9e35b2cb87ce04d05f0b6afef8c2d`  
		Last Modified: Wed, 01 Mar 2017 22:45:56 GMT  
		Size: 65.1 MB (65055354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3926b08578e0ea40880f0730ee8030603c3132c3a479d9a62923c128c4098971`  
		Last Modified: Wed, 01 Mar 2017 22:45:41 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a414a1469bcedd9a189d75a862a699d20ec990b49fdd27f08c4c26afbb25923`  
		Last Modified: Wed, 01 Mar 2017 22:45:41 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa5d9e5aeeebe131b96abd1eebb921abc7d9890e900cb7268df1e08e22c6f81`  
		Last Modified: Wed, 01 Mar 2017 22:45:41 GMT  
		Size: 123.2 KB (123203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db233e7f9c3dedc80952e1f673828c699593168c07dbb737254f53bff9a4f5f5`  
		Last Modified: Wed, 01 Mar 2017 22:45:39 GMT  
		Size: 807.6 KB (807588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d83a419005b9e75add3bb4e97dc4efedcec11c8d9d5895e98fa0a292eeb82e`  
		Last Modified: Wed, 01 Mar 2017 22:45:39 GMT  
		Size: 1.4 MB (1382493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a297a21c4102d50ad97c3511155e392f4e980bdb530343700ba37ce044a7eef3`  
		Last Modified: Wed, 01 Mar 2017 22:45:46 GMT  
		Size: 83.4 MB (83393762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93f05c78c9e693e078560b8ea0cf99e87628dead6148911f90a00fa5e5ae9da`  
		Last Modified: Wed, 01 Mar 2017 22:45:38 GMT  
		Size: 5.8 KB (5808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f6bec43f031db28da3c57227a7eccf10c08bf3919ac0a7ec0cfcc78d5c3289`  
		Last Modified: Wed, 01 Mar 2017 22:45:38 GMT  
		Size: 3.3 KB (3254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.4.2`

```console
$ docker pull bonita@sha256:f362565e265d95755d65b80010f64c5ea2f4e492bca543dc52e85876b43a215b
```

-	Platforms:
	-	linux; amd64

### `bonita:7.4.2` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 MB (216988682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0818c9baf6cf8950557cc411ae026c3d8ede699f814c7e5d55ad996b163762`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 27 Feb 2017 19:40:39 GMT
ADD file:a642bdc2d8d6e4484e4419fc938e24b03454e36f389233f2ce77fc04722da900 in / 
# Mon, 27 Feb 2017 19:40:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 27 Feb 2017 19:40:49 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 19:41:05 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Mon, 27 Feb 2017 19:41:06 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 27 Feb 2017 19:41:06 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 22:43:09 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Mon, 27 Feb 2017 22:44:00 GMT
RUN apt-get update && apt-get install -y   mysql-client-core-5.5   openjdk-7-jre-headless   postgresql-client   unzip   wget   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 22:44:00 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 27 Feb 2017 22:44:01 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 27 Feb 2017 22:44:03 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4
# Mon, 27 Feb 2017 22:44:07 GMT
RUN wget -q "https://github.com/tianon/gosu/releases/download/1.6/gosu-$(dpkg --print-architecture)" -O /usr/local/bin/gosu   && wget -q "https://github.com/tianon/gosu/releases/download/1.6/gosu-$(dpkg --print-architecture).asc" -O /usr/local/bin/gosu.asc   && gpg --verify /usr/local/bin/gosu.asc   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 27 Feb 2017 22:44:28 GMT
ENV BONITA_VERSION=7.4.2
# Mon, 27 Feb 2017 22:44:29 GMT
ENV TOMCAT_VERSION=7.0.67
# Mon, 27 Feb 2017 22:44:29 GMT
ENV BONITA_SHA256=62f489362ed273f700032f5da1b4dc70a4bc74c9add2cb27e6c3be50e1e284f6
# Mon, 27 Feb 2017 22:44:40 GMT
RUN mkdir /opt/files   && wget -q http://download.forge.ow2.org/bonita/BonitaBPMCommunity-${BONITA_VERSION}-Tomcat-${TOMCAT_VERSION}.zip -O /opt/files/BonitaBPMCommunity-${BONITA_VERSION}-Tomcat-${TOMCAT_VERSION}.zip   && echo "$BONITA_SHA256" /opt/files/BonitaBPMCommunity-${BONITA_VERSION}-Tomcat-${TOMCAT_VERSION}.zip | sha256sum -c -
# Mon, 27 Feb 2017 22:44:40 GMT
VOLUME [/opt/bonita]
# Mon, 27 Feb 2017 22:44:41 GMT
COPY dir:9a4e5e16ecaf38cc54b83e4c92a5f49851cda4f8d38d0cfe3c6a1849e3765b28 in /opt/files 
# Mon, 27 Feb 2017 22:44:41 GMT
COPY dir:0f5b28efb7aa0114806152fbcfef64599a58d3bd42d494d262f29d8f3408ea15 in /opt/templates 
# Mon, 27 Feb 2017 22:44:42 GMT
EXPOSE 8080/tcp
# Mon, 27 Feb 2017 22:44:42 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:30d541b48fc05d2a1b2b0ac6a74f3df70e928c3edc253d5bce5dc6ae1fad55d2`  
		Last Modified: Mon, 27 Feb 2017 19:46:55 GMT  
		Size: 65.7 MB (65693630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecd7f80d390b9e9a009363abea9fb2bb53e8104b4fc2f7abe00ee254005af1c`  
		Last Modified: Mon, 27 Feb 2017 19:46:34 GMT  
		Size: 71.6 KB (71555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ec9927bb81d07ac2602292888b2c61213d51d1a4eeef6354fb9734246e52da`  
		Last Modified: Mon, 27 Feb 2017 19:46:34 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e67a4d67b44968a2e2b40b1a22c6ad3192a9a490f1a47824f1309f8b97d30e5`  
		Last Modified: Mon, 27 Feb 2017 19:46:34 GMT  
		Size: 680.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9dd91554882183cb5d1cd512479487e10f495c22d035a62fbb3ee38d89cf48`  
		Last Modified: Mon, 27 Feb 2017 19:46:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8a9ece2ab54505896ac4c64bf6c03753f9e35b2cb87ce04d05f0b6afef8c2d`  
		Last Modified: Wed, 01 Mar 2017 22:45:56 GMT  
		Size: 65.1 MB (65055354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3926b08578e0ea40880f0730ee8030603c3132c3a479d9a62923c128c4098971`  
		Last Modified: Wed, 01 Mar 2017 22:45:41 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a414a1469bcedd9a189d75a862a699d20ec990b49fdd27f08c4c26afbb25923`  
		Last Modified: Wed, 01 Mar 2017 22:45:41 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa5d9e5aeeebe131b96abd1eebb921abc7d9890e900cb7268df1e08e22c6f81`  
		Last Modified: Wed, 01 Mar 2017 22:45:41 GMT  
		Size: 123.2 KB (123203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db233e7f9c3dedc80952e1f673828c699593168c07dbb737254f53bff9a4f5f5`  
		Last Modified: Wed, 01 Mar 2017 22:45:39 GMT  
		Size: 807.6 KB (807588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0154c060232abc8082b1a379107094ae1e96ed68ebe4cba5e7172fe896eba49`  
		Last Modified: Wed, 01 Mar 2017 22:46:27 GMT  
		Size: 85.2 MB (85226631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e403b93bf382e5a28d7adb4b4fa2b3ad31add01c6e4c4d39d7b56b53f39fca8`  
		Last Modified: Wed, 01 Mar 2017 22:46:20 GMT  
		Size: 6.0 KB (6013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387dc6c52a3ba4733986ea95b6d595f832c5288c62accbc3337f8ca56aea6180`  
		Last Modified: Wed, 01 Mar 2017 22:46:20 GMT  
		Size: 1.6 KB (1608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:f362565e265d95755d65b80010f64c5ea2f4e492bca543dc52e85876b43a215b
```

-	Platforms:
	-	linux; amd64

### `bonita:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 MB (216988682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0818c9baf6cf8950557cc411ae026c3d8ede699f814c7e5d55ad996b163762`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 27 Feb 2017 19:40:39 GMT
ADD file:a642bdc2d8d6e4484e4419fc938e24b03454e36f389233f2ce77fc04722da900 in / 
# Mon, 27 Feb 2017 19:40:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 27 Feb 2017 19:40:49 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 19:41:05 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Mon, 27 Feb 2017 19:41:06 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 27 Feb 2017 19:41:06 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 22:43:09 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Mon, 27 Feb 2017 22:44:00 GMT
RUN apt-get update && apt-get install -y   mysql-client-core-5.5   openjdk-7-jre-headless   postgresql-client   unzip   wget   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 22:44:00 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 27 Feb 2017 22:44:01 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 27 Feb 2017 22:44:03 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4
# Mon, 27 Feb 2017 22:44:07 GMT
RUN wget -q "https://github.com/tianon/gosu/releases/download/1.6/gosu-$(dpkg --print-architecture)" -O /usr/local/bin/gosu   && wget -q "https://github.com/tianon/gosu/releases/download/1.6/gosu-$(dpkg --print-architecture).asc" -O /usr/local/bin/gosu.asc   && gpg --verify /usr/local/bin/gosu.asc   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 27 Feb 2017 22:44:28 GMT
ENV BONITA_VERSION=7.4.2
# Mon, 27 Feb 2017 22:44:29 GMT
ENV TOMCAT_VERSION=7.0.67
# Mon, 27 Feb 2017 22:44:29 GMT
ENV BONITA_SHA256=62f489362ed273f700032f5da1b4dc70a4bc74c9add2cb27e6c3be50e1e284f6
# Mon, 27 Feb 2017 22:44:40 GMT
RUN mkdir /opt/files   && wget -q http://download.forge.ow2.org/bonita/BonitaBPMCommunity-${BONITA_VERSION}-Tomcat-${TOMCAT_VERSION}.zip -O /opt/files/BonitaBPMCommunity-${BONITA_VERSION}-Tomcat-${TOMCAT_VERSION}.zip   && echo "$BONITA_SHA256" /opt/files/BonitaBPMCommunity-${BONITA_VERSION}-Tomcat-${TOMCAT_VERSION}.zip | sha256sum -c -
# Mon, 27 Feb 2017 22:44:40 GMT
VOLUME [/opt/bonita]
# Mon, 27 Feb 2017 22:44:41 GMT
COPY dir:9a4e5e16ecaf38cc54b83e4c92a5f49851cda4f8d38d0cfe3c6a1849e3765b28 in /opt/files 
# Mon, 27 Feb 2017 22:44:41 GMT
COPY dir:0f5b28efb7aa0114806152fbcfef64599a58d3bd42d494d262f29d8f3408ea15 in /opt/templates 
# Mon, 27 Feb 2017 22:44:42 GMT
EXPOSE 8080/tcp
# Mon, 27 Feb 2017 22:44:42 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:30d541b48fc05d2a1b2b0ac6a74f3df70e928c3edc253d5bce5dc6ae1fad55d2`  
		Last Modified: Mon, 27 Feb 2017 19:46:55 GMT  
		Size: 65.7 MB (65693630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecd7f80d390b9e9a009363abea9fb2bb53e8104b4fc2f7abe00ee254005af1c`  
		Last Modified: Mon, 27 Feb 2017 19:46:34 GMT  
		Size: 71.6 KB (71555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ec9927bb81d07ac2602292888b2c61213d51d1a4eeef6354fb9734246e52da`  
		Last Modified: Mon, 27 Feb 2017 19:46:34 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e67a4d67b44968a2e2b40b1a22c6ad3192a9a490f1a47824f1309f8b97d30e5`  
		Last Modified: Mon, 27 Feb 2017 19:46:34 GMT  
		Size: 680.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9dd91554882183cb5d1cd512479487e10f495c22d035a62fbb3ee38d89cf48`  
		Last Modified: Mon, 27 Feb 2017 19:46:35 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8a9ece2ab54505896ac4c64bf6c03753f9e35b2cb87ce04d05f0b6afef8c2d`  
		Last Modified: Wed, 01 Mar 2017 22:45:56 GMT  
		Size: 65.1 MB (65055354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3926b08578e0ea40880f0730ee8030603c3132c3a479d9a62923c128c4098971`  
		Last Modified: Wed, 01 Mar 2017 22:45:41 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a414a1469bcedd9a189d75a862a699d20ec990b49fdd27f08c4c26afbb25923`  
		Last Modified: Wed, 01 Mar 2017 22:45:41 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa5d9e5aeeebe131b96abd1eebb921abc7d9890e900cb7268df1e08e22c6f81`  
		Last Modified: Wed, 01 Mar 2017 22:45:41 GMT  
		Size: 123.2 KB (123203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db233e7f9c3dedc80952e1f673828c699593168c07dbb737254f53bff9a4f5f5`  
		Last Modified: Wed, 01 Mar 2017 22:45:39 GMT  
		Size: 807.6 KB (807588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0154c060232abc8082b1a379107094ae1e96ed68ebe4cba5e7172fe896eba49`  
		Last Modified: Wed, 01 Mar 2017 22:46:27 GMT  
		Size: 85.2 MB (85226631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e403b93bf382e5a28d7adb4b4fa2b3ad31add01c6e4c4d39d7b56b53f39fca8`  
		Last Modified: Wed, 01 Mar 2017 22:46:20 GMT  
		Size: 6.0 KB (6013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387dc6c52a3ba4733986ea95b6d595f832c5288c62accbc3337f8ca56aea6180`  
		Last Modified: Wed, 01 Mar 2017 22:46:20 GMT  
		Size: 1.6 KB (1608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
