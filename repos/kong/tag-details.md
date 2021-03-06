<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:0.10`](#kong010)
-	[`kong:0.10.0`](#kong0100)
-	[`kong:latest`](#konglatest)

## `kong:0.10`

```console
$ docker pull kong@sha256:3d512b0e5d52442ca6b81dc3378c76068d8648a5d47359273be74da400115a96
```

-	Platforms:
	-	linux; amd64

### `kong:0.10` - linux; amd64

-	Docker Version: 1.12.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124222233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b8dc2217f7e1e54f2b2ef01ac51afcb1d953a9f6e8fb8ebd926cf03bca9fb7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","start"]`

```dockerfile
# Tue, 30 Aug 2016 18:18:45 GMT
MAINTAINER https://github.com/CentOS/sig-cloud-instance-images
# Thu, 15 Dec 2016 18:21:21 GMT
ADD file:940c77b6724c00d4208cc72169a63951eaa605672bcc5902ab2013cbae107434 in / 
# Thu, 15 Dec 2016 18:21:23 GMT
LABEL name=CentOS Base Image vendor=CentOS license=GPLv2 build-date=20161214
# Thu, 15 Dec 2016 18:21:23 GMT
CMD ["/bin/bash"]
# Thu, 15 Dec 2016 18:24:28 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Wed, 08 Mar 2017 18:37:05 GMT
ENV KONG_VERSION=0.10.0
# Wed, 08 Mar 2017 18:37:32 GMT
RUN yum install -y wget https://github.com/Mashape/kong/releases/download/$KONG_VERSION/kong-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Wed, 08 Mar 2017 18:37:35 GMT
RUN wget -O /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.1.3/dumb-init_1.1.3_amd64 &&     chmod +x /usr/local/bin/dumb-init
# Wed, 08 Mar 2017 18:37:36 GMT
COPY file:e806c057c1c71a8dd5e684244eed51d4ff17ca43efe7233573320a3bf8dda3a4 in /docker-entrypoint.sh 
# Wed, 08 Mar 2017 18:37:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Mar 2017 18:37:38 GMT
EXPOSE 7946/tcp 8000/tcp 8001/tcp 8443/tcp
# Wed, 08 Mar 2017 18:37:39 GMT
CMD ["kong" "start"]
```

-	Layers:
	-	`sha256:45a2e645736c4c66ef34acce2407ded21f7a9b231199d3b92d6c9776df264729`  
		Last Modified: Thu, 15 Dec 2016 18:22:30 GMT  
		Size: 70.4 MB (70389679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6050cc584d9fb511f6fdce5457f02ad02fa75f1c68ba2491eb08d06508bb768e`  
		Last Modified: Wed, 08 Mar 2017 18:37:58 GMT  
		Size: 53.8 MB (53807690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bb638dfd20254d8a191d26472afff1c3d77295169de04e043c66d1d0a21f0e`  
		Last Modified: Wed, 08 Mar 2017 18:37:44 GMT  
		Size: 24.6 KB (24643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b38426c48558a0d0f33605909aafd9dd13fa123db7b268bd083d5c26ec14b10`  
		Last Modified: Wed, 08 Mar 2017 18:37:44 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.10.0`

```console
$ docker pull kong@sha256:3d512b0e5d52442ca6b81dc3378c76068d8648a5d47359273be74da400115a96
```

-	Platforms:
	-	linux; amd64

### `kong:0.10.0` - linux; amd64

-	Docker Version: 1.12.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124222233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b8dc2217f7e1e54f2b2ef01ac51afcb1d953a9f6e8fb8ebd926cf03bca9fb7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","start"]`

```dockerfile
# Tue, 30 Aug 2016 18:18:45 GMT
MAINTAINER https://github.com/CentOS/sig-cloud-instance-images
# Thu, 15 Dec 2016 18:21:21 GMT
ADD file:940c77b6724c00d4208cc72169a63951eaa605672bcc5902ab2013cbae107434 in / 
# Thu, 15 Dec 2016 18:21:23 GMT
LABEL name=CentOS Base Image vendor=CentOS license=GPLv2 build-date=20161214
# Thu, 15 Dec 2016 18:21:23 GMT
CMD ["/bin/bash"]
# Thu, 15 Dec 2016 18:24:28 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Wed, 08 Mar 2017 18:37:05 GMT
ENV KONG_VERSION=0.10.0
# Wed, 08 Mar 2017 18:37:32 GMT
RUN yum install -y wget https://github.com/Mashape/kong/releases/download/$KONG_VERSION/kong-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Wed, 08 Mar 2017 18:37:35 GMT
RUN wget -O /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.1.3/dumb-init_1.1.3_amd64 &&     chmod +x /usr/local/bin/dumb-init
# Wed, 08 Mar 2017 18:37:36 GMT
COPY file:e806c057c1c71a8dd5e684244eed51d4ff17ca43efe7233573320a3bf8dda3a4 in /docker-entrypoint.sh 
# Wed, 08 Mar 2017 18:37:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Mar 2017 18:37:38 GMT
EXPOSE 7946/tcp 8000/tcp 8001/tcp 8443/tcp
# Wed, 08 Mar 2017 18:37:39 GMT
CMD ["kong" "start"]
```

-	Layers:
	-	`sha256:45a2e645736c4c66ef34acce2407ded21f7a9b231199d3b92d6c9776df264729`  
		Last Modified: Thu, 15 Dec 2016 18:22:30 GMT  
		Size: 70.4 MB (70389679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6050cc584d9fb511f6fdce5457f02ad02fa75f1c68ba2491eb08d06508bb768e`  
		Last Modified: Wed, 08 Mar 2017 18:37:58 GMT  
		Size: 53.8 MB (53807690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bb638dfd20254d8a191d26472afff1c3d77295169de04e043c66d1d0a21f0e`  
		Last Modified: Wed, 08 Mar 2017 18:37:44 GMT  
		Size: 24.6 KB (24643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b38426c48558a0d0f33605909aafd9dd13fa123db7b268bd083d5c26ec14b10`  
		Last Modified: Wed, 08 Mar 2017 18:37:44 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:3d512b0e5d52442ca6b81dc3378c76068d8648a5d47359273be74da400115a96
```

-	Platforms:
	-	linux; amd64

### `kong:latest` - linux; amd64

-	Docker Version: 1.12.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124222233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b8dc2217f7e1e54f2b2ef01ac51afcb1d953a9f6e8fb8ebd926cf03bca9fb7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","start"]`

```dockerfile
# Tue, 30 Aug 2016 18:18:45 GMT
MAINTAINER https://github.com/CentOS/sig-cloud-instance-images
# Thu, 15 Dec 2016 18:21:21 GMT
ADD file:940c77b6724c00d4208cc72169a63951eaa605672bcc5902ab2013cbae107434 in / 
# Thu, 15 Dec 2016 18:21:23 GMT
LABEL name=CentOS Base Image vendor=CentOS license=GPLv2 build-date=20161214
# Thu, 15 Dec 2016 18:21:23 GMT
CMD ["/bin/bash"]
# Thu, 15 Dec 2016 18:24:28 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Wed, 08 Mar 2017 18:37:05 GMT
ENV KONG_VERSION=0.10.0
# Wed, 08 Mar 2017 18:37:32 GMT
RUN yum install -y wget https://github.com/Mashape/kong/releases/download/$KONG_VERSION/kong-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Wed, 08 Mar 2017 18:37:35 GMT
RUN wget -O /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.1.3/dumb-init_1.1.3_amd64 &&     chmod +x /usr/local/bin/dumb-init
# Wed, 08 Mar 2017 18:37:36 GMT
COPY file:e806c057c1c71a8dd5e684244eed51d4ff17ca43efe7233573320a3bf8dda3a4 in /docker-entrypoint.sh 
# Wed, 08 Mar 2017 18:37:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 08 Mar 2017 18:37:38 GMT
EXPOSE 7946/tcp 8000/tcp 8001/tcp 8443/tcp
# Wed, 08 Mar 2017 18:37:39 GMT
CMD ["kong" "start"]
```

-	Layers:
	-	`sha256:45a2e645736c4c66ef34acce2407ded21f7a9b231199d3b92d6c9776df264729`  
		Last Modified: Thu, 15 Dec 2016 18:22:30 GMT  
		Size: 70.4 MB (70389679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6050cc584d9fb511f6fdce5457f02ad02fa75f1c68ba2491eb08d06508bb768e`  
		Last Modified: Wed, 08 Mar 2017 18:37:58 GMT  
		Size: 53.8 MB (53807690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bb638dfd20254d8a191d26472afff1c3d77295169de04e043c66d1d0a21f0e`  
		Last Modified: Wed, 08 Mar 2017 18:37:44 GMT  
		Size: 24.6 KB (24643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b38426c48558a0d0f33605909aafd9dd13fa123db7b268bd083d5c26ec14b10`  
		Last Modified: Wed, 08 Mar 2017 18:37:44 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
