## `rakudo-star:latest`

```console
$ docker pull rakudo-star@sha256:eac1ce2634c62857ee7e5e3f23b2156206edef779da47c08c4ac508f905ca60d
```

-	Platforms:
	-	linux; amd64

### `rakudo-star:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124050437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c55ff2dc88749dbd1643185bf278497491ce8baf0cdeb36271f986c9989d9d5`
-	Default Command: `["perl6"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:42:10 GMT
MAINTAINER Rob Hoelz
# Tue, 28 Feb 2017 22:42:11 GMT
RUN groupadd -r perl6 && useradd -r -g perl6 perl6
# Tue, 28 Feb 2017 22:42:11 GMT
ENV rakudo_version=2017.01
# Tue, 28 Feb 2017 22:49:50 GMT
RUN buildDeps='         gcc         libc6-dev         libencode-perl         make     '     && set -x     && apt-get update     && apt-get --yes install --no-install-recommends $buildDeps     && rm -rf /var/lib/apt/lists/*     && mkdir /root/rakudo     && curl -fsSL http://rakudo.org/downloads/star/rakudo-star-${rakudo_version}.tar.gz -o rakudo.tar.gz     && tar xzf rakudo.tar.gz --strip-components=1 -C /root/rakudo     && (         cd /root/rakudo         && perl Configure.pl --prefix=/usr --gen-moar         && make install     )     && rm -rf /rakudo.tar.gz /root/rakudo     && apt-get purge -y --auto-remove $buildDeps
# Tue, 28 Feb 2017 22:49:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/share/perl6/site/bin
# Tue, 28 Feb 2017 22:49:51 GMT
CMD ["perl6"]
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
	-	`sha256:5d2dc01312f3714eed4630a1317629f9131f307b3fc6d83506444d3eeebc0e41`  
		Last Modified: Mon, 27 Feb 2017 21:54:18 GMT  
		Size: 42.5 MB (42501192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e090aa29a3ecef06966794f34edbc21a4e335f0cf96cc901349528a1295752db`  
		Last Modified: Thu, 02 Mar 2017 03:35:44 GMT  
		Size: 2.1 KB (2054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3439586dbe8d43f25d6d99a622d092522d2563ae58172cc01eb63dcb4704b6b`  
		Last Modified: Thu, 02 Mar 2017 03:35:50 GMT  
		Size: 11.6 MB (11647822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
