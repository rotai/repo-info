<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `haxe`

-	[`haxe:3.1.3`](#haxe313)
-	[`haxe:3.1`](#haxe31)
-	[`haxe:3.1.3-onbuild`](#haxe313-onbuild)
-	[`haxe:3.1-onbuild`](#haxe31-onbuild)
-	[`haxe:3.2.1`](#haxe321)
-	[`haxe:3.2`](#haxe32)
-	[`haxe:3.2.1-onbuild`](#haxe321-onbuild)
-	[`haxe:3.2-onbuild`](#haxe32-onbuild)
-	[`haxe:3.3.0-rc.1`](#haxe330-rc1)
-	[`haxe:3.3.0`](#haxe330)
-	[`haxe:3.3`](#haxe33)
-	[`haxe:3.3.0-rc.1-onbuild`](#haxe330-rc1-onbuild)
-	[`haxe:3.3.0-onbuild`](#haxe330-onbuild)
-	[`haxe:3.3-onbuild`](#haxe33-onbuild)
-	[`haxe:3.4.0`](#haxe340)
-	[`haxe:3.4`](#haxe34)
-	[`haxe:latest`](#haxelatest)
-	[`haxe:3.4.0-onbuild`](#haxe340-onbuild)
-	[`haxe:3.4-onbuild`](#haxe34-onbuild)

## `haxe:3.1.3`

```console
$ docker pull haxe@sha256:7c773b87ee7231639bebd22efc8fbaa3935d25b3342a844fa96762205e5dc1a1
```

-	Platforms:
	-	linux; amd64

### `haxe:3.1.3` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118865429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85fdef9b396084b95d0c1fe4ec994e92d082b309f3501551086d7b48613ff93`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:30 GMT
ENV NEKO_VERSION=2.1.0
# Tue, 28 Feb 2017 03:25:31 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 28 Feb 2017 03:26:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "http://nekovm.org/media/neko-2.1.0-src.tar.gz" 	&& echo "0c93d5fe96240510e2d1975ae0caa9dd8eadf70d916a868684f66a099a4acf96 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 28 Feb 2017 03:26:48 GMT
ENV HAXE_VERSION=3.1.3
# Tue, 28 Feb 2017 03:27:38 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-native-compilers 		camlp4 		libxml-light-ocaml-dev 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& git clone --recursive --depth 1 --branch 3.1.3 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& make OCAMLOPT=ocamlopt.opt 	&& make install INSTALL_DIR=/usr/local 	&& cd / && haxelib setup /usr/local/lib/haxe/lib 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 28 Feb 2017 03:27:38 GMT
CMD ["haxe"]
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
	-	`sha256:7349211cd29341d185560f660c78499a748897b67eb58c08cb077843e742f2c6`  
		Last Modified: Thu, 02 Mar 2017 00:36:27 GMT  
		Size: 254.6 KB (254620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b7c094eb09fdafd36e2bf6648bd7feaa1f290daa4398625e1e1779d9892e38`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f1ae260490eff97ced26ab90532fd22598ebfc83296ab4a6c013fb920d33c3`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 2.2 MB (2191459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db478be9612778ef97e86701f286da175bc051ee249526e2b115b711dc3de4f`  
		Last Modified: Thu, 02 Mar 2017 00:36:32 GMT  
		Size: 4.0 MB (4018575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haxe:3.1`

```console
$ docker pull haxe@sha256:7c773b87ee7231639bebd22efc8fbaa3935d25b3342a844fa96762205e5dc1a1
```

-	Platforms:
	-	linux; amd64

### `haxe:3.1` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118865429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85fdef9b396084b95d0c1fe4ec994e92d082b309f3501551086d7b48613ff93`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:30 GMT
ENV NEKO_VERSION=2.1.0
# Tue, 28 Feb 2017 03:25:31 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 28 Feb 2017 03:26:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "http://nekovm.org/media/neko-2.1.0-src.tar.gz" 	&& echo "0c93d5fe96240510e2d1975ae0caa9dd8eadf70d916a868684f66a099a4acf96 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 28 Feb 2017 03:26:48 GMT
ENV HAXE_VERSION=3.1.3
# Tue, 28 Feb 2017 03:27:38 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-native-compilers 		camlp4 		libxml-light-ocaml-dev 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& git clone --recursive --depth 1 --branch 3.1.3 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& make OCAMLOPT=ocamlopt.opt 	&& make install INSTALL_DIR=/usr/local 	&& cd / && haxelib setup /usr/local/lib/haxe/lib 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 28 Feb 2017 03:27:38 GMT
CMD ["haxe"]
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
	-	`sha256:7349211cd29341d185560f660c78499a748897b67eb58c08cb077843e742f2c6`  
		Last Modified: Thu, 02 Mar 2017 00:36:27 GMT  
		Size: 254.6 KB (254620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b7c094eb09fdafd36e2bf6648bd7feaa1f290daa4398625e1e1779d9892e38`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f1ae260490eff97ced26ab90532fd22598ebfc83296ab4a6c013fb920d33c3`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 2.2 MB (2191459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db478be9612778ef97e86701f286da175bc051ee249526e2b115b711dc3de4f`  
		Last Modified: Thu, 02 Mar 2017 00:36:32 GMT  
		Size: 4.0 MB (4018575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haxe:3.1.3-onbuild`

```console
$ docker pull haxe@sha256:1d74984f95dcf6e506e4d29aced71988efe3335c5ea7c149c910e1c554e1fcc5
```

-	Platforms:
	-	linux; amd64

### `haxe:3.1.3-onbuild` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118865557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165961311963cbca948837ad0579d8b383d6d50af664d22506ce4f96f845bbe9`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:30 GMT
ENV NEKO_VERSION=2.1.0
# Tue, 28 Feb 2017 03:25:31 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 28 Feb 2017 03:26:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "http://nekovm.org/media/neko-2.1.0-src.tar.gz" 	&& echo "0c93d5fe96240510e2d1975ae0caa9dd8eadf70d916a868684f66a099a4acf96 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 28 Feb 2017 03:26:48 GMT
ENV HAXE_VERSION=3.1.3
# Tue, 28 Feb 2017 03:27:38 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-native-compilers 		camlp4 		libxml-light-ocaml-dev 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& git clone --recursive --depth 1 --branch 3.1.3 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& make OCAMLOPT=ocamlopt.opt 	&& make install INSTALL_DIR=/usr/local 	&& cd / && haxelib setup /usr/local/lib/haxe/lib 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 28 Feb 2017 03:27:38 GMT
CMD ["haxe"]
# Tue, 28 Feb 2017 03:27:39 GMT
RUN mkdir -p /usr/src/app
# Tue, 28 Feb 2017 03:27:40 GMT
WORKDIR /usr/src/app
# Tue, 28 Feb 2017 03:27:40 GMT
ONBUILD COPY *.hxml /usr/src/app/
# Tue, 28 Feb 2017 03:27:41 GMT
ONBUILD RUN yes | haxelib install all
# Tue, 28 Feb 2017 03:27:41 GMT
ONBUILD COPY . /usr/src/app
# Tue, 28 Feb 2017 03:27:41 GMT
ONBUILD ARG BUILD_HXML=build.hxml
# Tue, 28 Feb 2017 03:27:42 GMT
ONBUILD RUN haxe $BUILD_HXML
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
	-	`sha256:7349211cd29341d185560f660c78499a748897b67eb58c08cb077843e742f2c6`  
		Last Modified: Thu, 02 Mar 2017 00:36:27 GMT  
		Size: 254.6 KB (254620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b7c094eb09fdafd36e2bf6648bd7feaa1f290daa4398625e1e1779d9892e38`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f1ae260490eff97ced26ab90532fd22598ebfc83296ab4a6c013fb920d33c3`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 2.2 MB (2191459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db478be9612778ef97e86701f286da175bc051ee249526e2b115b711dc3de4f`  
		Last Modified: Thu, 02 Mar 2017 00:36:32 GMT  
		Size: 4.0 MB (4018575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c2cfb3f00b494471ef35dca690e9749807c70c966fa64450a1f8f65c314a28`  
		Last Modified: Thu, 02 Mar 2017 00:37:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haxe:3.1-onbuild`

```console
$ docker pull haxe@sha256:1d74984f95dcf6e506e4d29aced71988efe3335c5ea7c149c910e1c554e1fcc5
```

-	Platforms:
	-	linux; amd64

### `haxe:3.1-onbuild` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118865557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165961311963cbca948837ad0579d8b383d6d50af664d22506ce4f96f845bbe9`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:30 GMT
ENV NEKO_VERSION=2.1.0
# Tue, 28 Feb 2017 03:25:31 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 28 Feb 2017 03:26:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "http://nekovm.org/media/neko-2.1.0-src.tar.gz" 	&& echo "0c93d5fe96240510e2d1975ae0caa9dd8eadf70d916a868684f66a099a4acf96 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 28 Feb 2017 03:26:48 GMT
ENV HAXE_VERSION=3.1.3
# Tue, 28 Feb 2017 03:27:38 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-native-compilers 		camlp4 		libxml-light-ocaml-dev 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& git clone --recursive --depth 1 --branch 3.1.3 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& make OCAMLOPT=ocamlopt.opt 	&& make install INSTALL_DIR=/usr/local 	&& cd / && haxelib setup /usr/local/lib/haxe/lib 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 28 Feb 2017 03:27:38 GMT
CMD ["haxe"]
# Tue, 28 Feb 2017 03:27:39 GMT
RUN mkdir -p /usr/src/app
# Tue, 28 Feb 2017 03:27:40 GMT
WORKDIR /usr/src/app
# Tue, 28 Feb 2017 03:27:40 GMT
ONBUILD COPY *.hxml /usr/src/app/
# Tue, 28 Feb 2017 03:27:41 GMT
ONBUILD RUN yes | haxelib install all
# Tue, 28 Feb 2017 03:27:41 GMT
ONBUILD COPY . /usr/src/app
# Tue, 28 Feb 2017 03:27:41 GMT
ONBUILD ARG BUILD_HXML=build.hxml
# Tue, 28 Feb 2017 03:27:42 GMT
ONBUILD RUN haxe $BUILD_HXML
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
	-	`sha256:7349211cd29341d185560f660c78499a748897b67eb58c08cb077843e742f2c6`  
		Last Modified: Thu, 02 Mar 2017 00:36:27 GMT  
		Size: 254.6 KB (254620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b7c094eb09fdafd36e2bf6648bd7feaa1f290daa4398625e1e1779d9892e38`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f1ae260490eff97ced26ab90532fd22598ebfc83296ab4a6c013fb920d33c3`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 2.2 MB (2191459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db478be9612778ef97e86701f286da175bc051ee249526e2b115b711dc3de4f`  
		Last Modified: Thu, 02 Mar 2017 00:36:32 GMT  
		Size: 4.0 MB (4018575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c2cfb3f00b494471ef35dca690e9749807c70c966fa64450a1f8f65c314a28`  
		Last Modified: Thu, 02 Mar 2017 00:37:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haxe:3.2.1`

```console
$ docker pull haxe@sha256:ed579775ab8476c5c75d72dea2af49753e2bcdd59b45d4e1acaa61c94cf3ff8a
```

-	Platforms:
	-	linux; amd64

### `haxe:3.2.1` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119150130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b26ba94b02d4339fe73937d1c60e6dc713d9b1f310696a947ebc013889ddbe`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:30 GMT
ENV NEKO_VERSION=2.1.0
# Tue, 28 Feb 2017 03:25:31 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 28 Feb 2017 03:26:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "http://nekovm.org/media/neko-2.1.0-src.tar.gz" 	&& echo "0c93d5fe96240510e2d1975ae0caa9dd8eadf70d916a868684f66a099a4acf96 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 28 Feb 2017 03:27:42 GMT
ENV HAXE_VERSION=3.2.1
# Tue, 28 Feb 2017 03:28:29 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-native-compilers 		camlp4 		libxml-light-ocaml-dev 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& git clone --recursive --depth 1 --branch 3.2.1 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& make OCAMLOPT=ocamlopt.opt 	&& make install INSTALL_DIR=/usr/local 	&& cd / && haxelib setup /usr/local/lib/haxe/lib 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 28 Feb 2017 03:28:29 GMT
CMD ["haxe"]
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
	-	`sha256:7349211cd29341d185560f660c78499a748897b67eb58c08cb077843e742f2c6`  
		Last Modified: Thu, 02 Mar 2017 00:36:27 GMT  
		Size: 254.6 KB (254620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b7c094eb09fdafd36e2bf6648bd7feaa1f290daa4398625e1e1779d9892e38`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f1ae260490eff97ced26ab90532fd22598ebfc83296ab4a6c013fb920d33c3`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 2.2 MB (2191459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4096919dad90d88f2ad031b01eb1f31491bc45222e14cf613cbb871847e6a92`  
		Last Modified: Thu, 02 Mar 2017 00:38:30 GMT  
		Size: 4.3 MB (4303276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haxe:3.2`

```console
$ docker pull haxe@sha256:ed579775ab8476c5c75d72dea2af49753e2bcdd59b45d4e1acaa61c94cf3ff8a
```

-	Platforms:
	-	linux; amd64

### `haxe:3.2` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119150130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b26ba94b02d4339fe73937d1c60e6dc713d9b1f310696a947ebc013889ddbe`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:30 GMT
ENV NEKO_VERSION=2.1.0
# Tue, 28 Feb 2017 03:25:31 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 28 Feb 2017 03:26:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "http://nekovm.org/media/neko-2.1.0-src.tar.gz" 	&& echo "0c93d5fe96240510e2d1975ae0caa9dd8eadf70d916a868684f66a099a4acf96 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 28 Feb 2017 03:27:42 GMT
ENV HAXE_VERSION=3.2.1
# Tue, 28 Feb 2017 03:28:29 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-native-compilers 		camlp4 		libxml-light-ocaml-dev 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& git clone --recursive --depth 1 --branch 3.2.1 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& make OCAMLOPT=ocamlopt.opt 	&& make install INSTALL_DIR=/usr/local 	&& cd / && haxelib setup /usr/local/lib/haxe/lib 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 28 Feb 2017 03:28:29 GMT
CMD ["haxe"]
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
	-	`sha256:7349211cd29341d185560f660c78499a748897b67eb58c08cb077843e742f2c6`  
		Last Modified: Thu, 02 Mar 2017 00:36:27 GMT  
		Size: 254.6 KB (254620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b7c094eb09fdafd36e2bf6648bd7feaa1f290daa4398625e1e1779d9892e38`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f1ae260490eff97ced26ab90532fd22598ebfc83296ab4a6c013fb920d33c3`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 2.2 MB (2191459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4096919dad90d88f2ad031b01eb1f31491bc45222e14cf613cbb871847e6a92`  
		Last Modified: Thu, 02 Mar 2017 00:38:30 GMT  
		Size: 4.3 MB (4303276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haxe:3.2.1-onbuild`

```console
$ docker pull haxe@sha256:31b60e70222b4140882f54c44272e8d60d2841474f711ea51a1545258161305c
```

-	Platforms:
	-	linux; amd64

### `haxe:3.2.1-onbuild` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119150256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea8401d0ab458bf55d40cd1fd6b67096a71ff630c39fcc11b8132fd743491d5`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:30 GMT
ENV NEKO_VERSION=2.1.0
# Tue, 28 Feb 2017 03:25:31 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 28 Feb 2017 03:26:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "http://nekovm.org/media/neko-2.1.0-src.tar.gz" 	&& echo "0c93d5fe96240510e2d1975ae0caa9dd8eadf70d916a868684f66a099a4acf96 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 28 Feb 2017 03:27:42 GMT
ENV HAXE_VERSION=3.2.1
# Tue, 28 Feb 2017 03:28:29 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-native-compilers 		camlp4 		libxml-light-ocaml-dev 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& git clone --recursive --depth 1 --branch 3.2.1 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& make OCAMLOPT=ocamlopt.opt 	&& make install INSTALL_DIR=/usr/local 	&& cd / && haxelib setup /usr/local/lib/haxe/lib 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 28 Feb 2017 03:28:29 GMT
CMD ["haxe"]
# Tue, 28 Feb 2017 03:28:30 GMT
RUN mkdir -p /usr/src/app
# Tue, 28 Feb 2017 03:28:31 GMT
WORKDIR /usr/src/app
# Tue, 28 Feb 2017 03:28:31 GMT
ONBUILD COPY *.hxml /usr/src/app/
# Tue, 28 Feb 2017 03:28:31 GMT
ONBUILD RUN yes | haxelib install all
# Tue, 28 Feb 2017 03:28:32 GMT
ONBUILD COPY . /usr/src/app
# Tue, 28 Feb 2017 03:28:32 GMT
ONBUILD ARG BUILD_HXML=build.hxml
# Tue, 28 Feb 2017 03:28:32 GMT
ONBUILD RUN haxe $BUILD_HXML
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
	-	`sha256:7349211cd29341d185560f660c78499a748897b67eb58c08cb077843e742f2c6`  
		Last Modified: Thu, 02 Mar 2017 00:36:27 GMT  
		Size: 254.6 KB (254620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b7c094eb09fdafd36e2bf6648bd7feaa1f290daa4398625e1e1779d9892e38`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f1ae260490eff97ced26ab90532fd22598ebfc83296ab4a6c013fb920d33c3`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 2.2 MB (2191459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4096919dad90d88f2ad031b01eb1f31491bc45222e14cf613cbb871847e6a92`  
		Last Modified: Thu, 02 Mar 2017 00:38:30 GMT  
		Size: 4.3 MB (4303276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed67e843658454b48eee6c8f982d35b9db90cad3e4d9c98fc801d8c7674f3e1a`  
		Last Modified: Thu, 02 Mar 2017 00:39:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haxe:3.2-onbuild`

```console
$ docker pull haxe@sha256:31b60e70222b4140882f54c44272e8d60d2841474f711ea51a1545258161305c
```

-	Platforms:
	-	linux; amd64

### `haxe:3.2-onbuild` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.2 MB (119150256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea8401d0ab458bf55d40cd1fd6b67096a71ff630c39fcc11b8132fd743491d5`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:30 GMT
ENV NEKO_VERSION=2.1.0
# Tue, 28 Feb 2017 03:25:31 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 28 Feb 2017 03:26:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "http://nekovm.org/media/neko-2.1.0-src.tar.gz" 	&& echo "0c93d5fe96240510e2d1975ae0caa9dd8eadf70d916a868684f66a099a4acf96 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 28 Feb 2017 03:27:42 GMT
ENV HAXE_VERSION=3.2.1
# Tue, 28 Feb 2017 03:28:29 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-native-compilers 		camlp4 		libxml-light-ocaml-dev 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& git clone --recursive --depth 1 --branch 3.2.1 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& make OCAMLOPT=ocamlopt.opt 	&& make install INSTALL_DIR=/usr/local 	&& cd / && haxelib setup /usr/local/lib/haxe/lib 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 28 Feb 2017 03:28:29 GMT
CMD ["haxe"]
# Tue, 28 Feb 2017 03:28:30 GMT
RUN mkdir -p /usr/src/app
# Tue, 28 Feb 2017 03:28:31 GMT
WORKDIR /usr/src/app
# Tue, 28 Feb 2017 03:28:31 GMT
ONBUILD COPY *.hxml /usr/src/app/
# Tue, 28 Feb 2017 03:28:31 GMT
ONBUILD RUN yes | haxelib install all
# Tue, 28 Feb 2017 03:28:32 GMT
ONBUILD COPY . /usr/src/app
# Tue, 28 Feb 2017 03:28:32 GMT
ONBUILD ARG BUILD_HXML=build.hxml
# Tue, 28 Feb 2017 03:28:32 GMT
ONBUILD RUN haxe $BUILD_HXML
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
	-	`sha256:7349211cd29341d185560f660c78499a748897b67eb58c08cb077843e742f2c6`  
		Last Modified: Thu, 02 Mar 2017 00:36:27 GMT  
		Size: 254.6 KB (254620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b7c094eb09fdafd36e2bf6648bd7feaa1f290daa4398625e1e1779d9892e38`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f1ae260490eff97ced26ab90532fd22598ebfc83296ab4a6c013fb920d33c3`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 2.2 MB (2191459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4096919dad90d88f2ad031b01eb1f31491bc45222e14cf613cbb871847e6a92`  
		Last Modified: Thu, 02 Mar 2017 00:38:30 GMT  
		Size: 4.3 MB (4303276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed67e843658454b48eee6c8f982d35b9db90cad3e4d9c98fc801d8c7674f3e1a`  
		Last Modified: Thu, 02 Mar 2017 00:39:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haxe:3.3.0-rc.1`

```console
$ docker pull haxe@sha256:eb5b5a3255347212f41c62fe9462ebcb3181e47edb7e4c762099d815f16ce732
```

-	Platforms:
	-	linux; amd64

### `haxe:3.3.0-rc.1` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120079094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d8d620a3e714b5e517b11b7aabeaf3117730a2716630301c55f92260f691ae`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:30 GMT
ENV NEKO_VERSION=2.1.0
# Tue, 28 Feb 2017 03:25:31 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 28 Feb 2017 03:26:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "http://nekovm.org/media/neko-2.1.0-src.tar.gz" 	&& echo "0c93d5fe96240510e2d1975ae0caa9dd8eadf70d916a868684f66a099a4acf96 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 28 Feb 2017 03:28:33 GMT
ENV HAXE_VERSION=3.3.0-rc.1
# Tue, 28 Feb 2017 03:29:22 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-native-compilers 		camlp4 		libxml-light-ocaml-dev 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& git clone --recursive --depth 1 --branch 3.3.0-rc1 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& make OCAMLOPT=ocamlopt.opt 	&& make install INSTALL_DIR=/usr/local 	&& cd / && haxelib setup /usr/local/lib/haxe/lib 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 28 Feb 2017 03:29:22 GMT
CMD ["haxe"]
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
	-	`sha256:7349211cd29341d185560f660c78499a748897b67eb58c08cb077843e742f2c6`  
		Last Modified: Thu, 02 Mar 2017 00:36:27 GMT  
		Size: 254.6 KB (254620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b7c094eb09fdafd36e2bf6648bd7feaa1f290daa4398625e1e1779d9892e38`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f1ae260490eff97ced26ab90532fd22598ebfc83296ab4a6c013fb920d33c3`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 2.2 MB (2191459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2517be739d16162ef4cd283883c24f027f5d18ede1d5c08db9864c1fd8d75351`  
		Last Modified: Thu, 02 Mar 2017 00:40:03 GMT  
		Size: 5.2 MB (5232240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haxe:3.3.0`

```console
$ docker pull haxe@sha256:eb5b5a3255347212f41c62fe9462ebcb3181e47edb7e4c762099d815f16ce732
```

-	Platforms:
	-	linux; amd64

### `haxe:3.3.0` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120079094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d8d620a3e714b5e517b11b7aabeaf3117730a2716630301c55f92260f691ae`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:30 GMT
ENV NEKO_VERSION=2.1.0
# Tue, 28 Feb 2017 03:25:31 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 28 Feb 2017 03:26:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "http://nekovm.org/media/neko-2.1.0-src.tar.gz" 	&& echo "0c93d5fe96240510e2d1975ae0caa9dd8eadf70d916a868684f66a099a4acf96 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 28 Feb 2017 03:28:33 GMT
ENV HAXE_VERSION=3.3.0-rc.1
# Tue, 28 Feb 2017 03:29:22 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-native-compilers 		camlp4 		libxml-light-ocaml-dev 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& git clone --recursive --depth 1 --branch 3.3.0-rc1 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& make OCAMLOPT=ocamlopt.opt 	&& make install INSTALL_DIR=/usr/local 	&& cd / && haxelib setup /usr/local/lib/haxe/lib 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 28 Feb 2017 03:29:22 GMT
CMD ["haxe"]
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
	-	`sha256:7349211cd29341d185560f660c78499a748897b67eb58c08cb077843e742f2c6`  
		Last Modified: Thu, 02 Mar 2017 00:36:27 GMT  
		Size: 254.6 KB (254620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b7c094eb09fdafd36e2bf6648bd7feaa1f290daa4398625e1e1779d9892e38`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f1ae260490eff97ced26ab90532fd22598ebfc83296ab4a6c013fb920d33c3`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 2.2 MB (2191459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2517be739d16162ef4cd283883c24f027f5d18ede1d5c08db9864c1fd8d75351`  
		Last Modified: Thu, 02 Mar 2017 00:40:03 GMT  
		Size: 5.2 MB (5232240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haxe:3.3`

```console
$ docker pull haxe@sha256:eb5b5a3255347212f41c62fe9462ebcb3181e47edb7e4c762099d815f16ce732
```

-	Platforms:
	-	linux; amd64

### `haxe:3.3` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120079094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d8d620a3e714b5e517b11b7aabeaf3117730a2716630301c55f92260f691ae`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:30 GMT
ENV NEKO_VERSION=2.1.0
# Tue, 28 Feb 2017 03:25:31 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 28 Feb 2017 03:26:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "http://nekovm.org/media/neko-2.1.0-src.tar.gz" 	&& echo "0c93d5fe96240510e2d1975ae0caa9dd8eadf70d916a868684f66a099a4acf96 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 28 Feb 2017 03:28:33 GMT
ENV HAXE_VERSION=3.3.0-rc.1
# Tue, 28 Feb 2017 03:29:22 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-native-compilers 		camlp4 		libxml-light-ocaml-dev 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& git clone --recursive --depth 1 --branch 3.3.0-rc1 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& make OCAMLOPT=ocamlopt.opt 	&& make install INSTALL_DIR=/usr/local 	&& cd / && haxelib setup /usr/local/lib/haxe/lib 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 28 Feb 2017 03:29:22 GMT
CMD ["haxe"]
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
	-	`sha256:7349211cd29341d185560f660c78499a748897b67eb58c08cb077843e742f2c6`  
		Last Modified: Thu, 02 Mar 2017 00:36:27 GMT  
		Size: 254.6 KB (254620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b7c094eb09fdafd36e2bf6648bd7feaa1f290daa4398625e1e1779d9892e38`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f1ae260490eff97ced26ab90532fd22598ebfc83296ab4a6c013fb920d33c3`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 2.2 MB (2191459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2517be739d16162ef4cd283883c24f027f5d18ede1d5c08db9864c1fd8d75351`  
		Last Modified: Thu, 02 Mar 2017 00:40:03 GMT  
		Size: 5.2 MB (5232240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haxe:3.3.0-rc.1-onbuild`

```console
$ docker pull haxe@sha256:2a48b015027b4bee759ce94e50716b84f0d26f691c49a59caa5180220c71abe3
```

-	Platforms:
	-	linux; amd64

### `haxe:3.3.0-rc.1-onbuild` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120079221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79af86d967c82af30740c9ddd486046897365281c371048b44220c8022a7c213`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:30 GMT
ENV NEKO_VERSION=2.1.0
# Tue, 28 Feb 2017 03:25:31 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 28 Feb 2017 03:26:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "http://nekovm.org/media/neko-2.1.0-src.tar.gz" 	&& echo "0c93d5fe96240510e2d1975ae0caa9dd8eadf70d916a868684f66a099a4acf96 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 28 Feb 2017 03:28:33 GMT
ENV HAXE_VERSION=3.3.0-rc.1
# Tue, 28 Feb 2017 03:29:22 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-native-compilers 		camlp4 		libxml-light-ocaml-dev 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& git clone --recursive --depth 1 --branch 3.3.0-rc1 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& make OCAMLOPT=ocamlopt.opt 	&& make install INSTALL_DIR=/usr/local 	&& cd / && haxelib setup /usr/local/lib/haxe/lib 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 28 Feb 2017 03:29:22 GMT
CMD ["haxe"]
# Tue, 28 Feb 2017 03:29:24 GMT
RUN mkdir -p /usr/src/app
# Tue, 28 Feb 2017 03:29:24 GMT
WORKDIR /usr/src/app
# Tue, 28 Feb 2017 03:29:24 GMT
ONBUILD COPY *.hxml /usr/src/app/
# Tue, 28 Feb 2017 03:29:25 GMT
ONBUILD RUN yes | haxelib install all
# Tue, 28 Feb 2017 03:29:25 GMT
ONBUILD COPY . /usr/src/app
# Tue, 28 Feb 2017 03:29:25 GMT
ONBUILD ARG BUILD_HXML=build.hxml
# Tue, 28 Feb 2017 03:29:26 GMT
ONBUILD RUN haxe $BUILD_HXML
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
	-	`sha256:7349211cd29341d185560f660c78499a748897b67eb58c08cb077843e742f2c6`  
		Last Modified: Thu, 02 Mar 2017 00:36:27 GMT  
		Size: 254.6 KB (254620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b7c094eb09fdafd36e2bf6648bd7feaa1f290daa4398625e1e1779d9892e38`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f1ae260490eff97ced26ab90532fd22598ebfc83296ab4a6c013fb920d33c3`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 2.2 MB (2191459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2517be739d16162ef4cd283883c24f027f5d18ede1d5c08db9864c1fd8d75351`  
		Last Modified: Thu, 02 Mar 2017 00:40:03 GMT  
		Size: 5.2 MB (5232240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7873f6279307b9627b55c79588196d2227da331ebe7ee85f22767d7500794c6d`  
		Last Modified: Thu, 02 Mar 2017 00:41:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haxe:3.3.0-onbuild`

```console
$ docker pull haxe@sha256:2a48b015027b4bee759ce94e50716b84f0d26f691c49a59caa5180220c71abe3
```

-	Platforms:
	-	linux; amd64

### `haxe:3.3.0-onbuild` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120079221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79af86d967c82af30740c9ddd486046897365281c371048b44220c8022a7c213`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:30 GMT
ENV NEKO_VERSION=2.1.0
# Tue, 28 Feb 2017 03:25:31 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 28 Feb 2017 03:26:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "http://nekovm.org/media/neko-2.1.0-src.tar.gz" 	&& echo "0c93d5fe96240510e2d1975ae0caa9dd8eadf70d916a868684f66a099a4acf96 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 28 Feb 2017 03:28:33 GMT
ENV HAXE_VERSION=3.3.0-rc.1
# Tue, 28 Feb 2017 03:29:22 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-native-compilers 		camlp4 		libxml-light-ocaml-dev 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& git clone --recursive --depth 1 --branch 3.3.0-rc1 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& make OCAMLOPT=ocamlopt.opt 	&& make install INSTALL_DIR=/usr/local 	&& cd / && haxelib setup /usr/local/lib/haxe/lib 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 28 Feb 2017 03:29:22 GMT
CMD ["haxe"]
# Tue, 28 Feb 2017 03:29:24 GMT
RUN mkdir -p /usr/src/app
# Tue, 28 Feb 2017 03:29:24 GMT
WORKDIR /usr/src/app
# Tue, 28 Feb 2017 03:29:24 GMT
ONBUILD COPY *.hxml /usr/src/app/
# Tue, 28 Feb 2017 03:29:25 GMT
ONBUILD RUN yes | haxelib install all
# Tue, 28 Feb 2017 03:29:25 GMT
ONBUILD COPY . /usr/src/app
# Tue, 28 Feb 2017 03:29:25 GMT
ONBUILD ARG BUILD_HXML=build.hxml
# Tue, 28 Feb 2017 03:29:26 GMT
ONBUILD RUN haxe $BUILD_HXML
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
	-	`sha256:7349211cd29341d185560f660c78499a748897b67eb58c08cb077843e742f2c6`  
		Last Modified: Thu, 02 Mar 2017 00:36:27 GMT  
		Size: 254.6 KB (254620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b7c094eb09fdafd36e2bf6648bd7feaa1f290daa4398625e1e1779d9892e38`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f1ae260490eff97ced26ab90532fd22598ebfc83296ab4a6c013fb920d33c3`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 2.2 MB (2191459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2517be739d16162ef4cd283883c24f027f5d18ede1d5c08db9864c1fd8d75351`  
		Last Modified: Thu, 02 Mar 2017 00:40:03 GMT  
		Size: 5.2 MB (5232240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7873f6279307b9627b55c79588196d2227da331ebe7ee85f22767d7500794c6d`  
		Last Modified: Thu, 02 Mar 2017 00:41:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haxe:3.3-onbuild`

```console
$ docker pull haxe@sha256:2a48b015027b4bee759ce94e50716b84f0d26f691c49a59caa5180220c71abe3
```

-	Platforms:
	-	linux; amd64

### `haxe:3.3-onbuild` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120079221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79af86d967c82af30740c9ddd486046897365281c371048b44220c8022a7c213`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:30 GMT
ENV NEKO_VERSION=2.1.0
# Tue, 28 Feb 2017 03:25:31 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 28 Feb 2017 03:26:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "http://nekovm.org/media/neko-2.1.0-src.tar.gz" 	&& echo "0c93d5fe96240510e2d1975ae0caa9dd8eadf70d916a868684f66a099a4acf96 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 28 Feb 2017 03:28:33 GMT
ENV HAXE_VERSION=3.3.0-rc.1
# Tue, 28 Feb 2017 03:29:22 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-native-compilers 		camlp4 		libxml-light-ocaml-dev 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& git clone --recursive --depth 1 --branch 3.3.0-rc1 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& make OCAMLOPT=ocamlopt.opt 	&& make install INSTALL_DIR=/usr/local 	&& cd / && haxelib setup /usr/local/lib/haxe/lib 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 28 Feb 2017 03:29:22 GMT
CMD ["haxe"]
# Tue, 28 Feb 2017 03:29:24 GMT
RUN mkdir -p /usr/src/app
# Tue, 28 Feb 2017 03:29:24 GMT
WORKDIR /usr/src/app
# Tue, 28 Feb 2017 03:29:24 GMT
ONBUILD COPY *.hxml /usr/src/app/
# Tue, 28 Feb 2017 03:29:25 GMT
ONBUILD RUN yes | haxelib install all
# Tue, 28 Feb 2017 03:29:25 GMT
ONBUILD COPY . /usr/src/app
# Tue, 28 Feb 2017 03:29:25 GMT
ONBUILD ARG BUILD_HXML=build.hxml
# Tue, 28 Feb 2017 03:29:26 GMT
ONBUILD RUN haxe $BUILD_HXML
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
	-	`sha256:7349211cd29341d185560f660c78499a748897b67eb58c08cb077843e742f2c6`  
		Last Modified: Thu, 02 Mar 2017 00:36:27 GMT  
		Size: 254.6 KB (254620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b7c094eb09fdafd36e2bf6648bd7feaa1f290daa4398625e1e1779d9892e38`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f1ae260490eff97ced26ab90532fd22598ebfc83296ab4a6c013fb920d33c3`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 2.2 MB (2191459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2517be739d16162ef4cd283883c24f027f5d18ede1d5c08db9864c1fd8d75351`  
		Last Modified: Thu, 02 Mar 2017 00:40:03 GMT  
		Size: 5.2 MB (5232240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7873f6279307b9627b55c79588196d2227da331ebe7ee85f22767d7500794c6d`  
		Last Modified: Thu, 02 Mar 2017 00:41:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haxe:3.4.0`

```console
$ docker pull haxe@sha256:23122931270ff8bbe6d51e15783110ef36529f7ffcdc7169020dac96ec8846f2
```

-	Platforms:
	-	linux; amd64

### `haxe:3.4.0` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120566776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4402a5a14128ec81219885a5442d6fbbc5e7d710763ed406ccdb3ed4f67ce9b`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:30 GMT
ENV NEKO_VERSION=2.1.0
# Tue, 28 Feb 2017 03:25:31 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 28 Feb 2017 03:26:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "http://nekovm.org/media/neko-2.1.0-src.tar.gz" 	&& echo "0c93d5fe96240510e2d1975ae0caa9dd8eadf70d916a868684f66a099a4acf96 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 28 Feb 2017 03:29:26 GMT
ENV HAXE_VERSION=3.4.0
# Tue, 28 Feb 2017 03:30:17 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-native-compilers 		camlp4 		libxml-light-ocaml-dev 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& git clone --recursive --depth 1 --branch 3.4.0 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& make OCAMLOPT=ocamlopt.opt 	&& make install INSTALL_DIR=/usr/local 	&& cd / && haxelib setup /usr/local/lib/haxe/lib 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 28 Feb 2017 03:30:18 GMT
CMD ["haxe"]
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
	-	`sha256:7349211cd29341d185560f660c78499a748897b67eb58c08cb077843e742f2c6`  
		Last Modified: Thu, 02 Mar 2017 00:36:27 GMT  
		Size: 254.6 KB (254620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b7c094eb09fdafd36e2bf6648bd7feaa1f290daa4398625e1e1779d9892e38`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f1ae260490eff97ced26ab90532fd22598ebfc83296ab4a6c013fb920d33c3`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 2.2 MB (2191459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4eafa440bd1dec3eca7079c7aafc7963304ecb2fdddfc1beab489c3a5cb7bed`  
		Last Modified: Thu, 02 Mar 2017 00:42:45 GMT  
		Size: 5.7 MB (5719922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haxe:3.4`

```console
$ docker pull haxe@sha256:23122931270ff8bbe6d51e15783110ef36529f7ffcdc7169020dac96ec8846f2
```

-	Platforms:
	-	linux; amd64

### `haxe:3.4` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120566776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4402a5a14128ec81219885a5442d6fbbc5e7d710763ed406ccdb3ed4f67ce9b`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:30 GMT
ENV NEKO_VERSION=2.1.0
# Tue, 28 Feb 2017 03:25:31 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 28 Feb 2017 03:26:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "http://nekovm.org/media/neko-2.1.0-src.tar.gz" 	&& echo "0c93d5fe96240510e2d1975ae0caa9dd8eadf70d916a868684f66a099a4acf96 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 28 Feb 2017 03:29:26 GMT
ENV HAXE_VERSION=3.4.0
# Tue, 28 Feb 2017 03:30:17 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-native-compilers 		camlp4 		libxml-light-ocaml-dev 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& git clone --recursive --depth 1 --branch 3.4.0 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& make OCAMLOPT=ocamlopt.opt 	&& make install INSTALL_DIR=/usr/local 	&& cd / && haxelib setup /usr/local/lib/haxe/lib 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 28 Feb 2017 03:30:18 GMT
CMD ["haxe"]
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
	-	`sha256:7349211cd29341d185560f660c78499a748897b67eb58c08cb077843e742f2c6`  
		Last Modified: Thu, 02 Mar 2017 00:36:27 GMT  
		Size: 254.6 KB (254620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b7c094eb09fdafd36e2bf6648bd7feaa1f290daa4398625e1e1779d9892e38`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f1ae260490eff97ced26ab90532fd22598ebfc83296ab4a6c013fb920d33c3`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 2.2 MB (2191459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4eafa440bd1dec3eca7079c7aafc7963304ecb2fdddfc1beab489c3a5cb7bed`  
		Last Modified: Thu, 02 Mar 2017 00:42:45 GMT  
		Size: 5.7 MB (5719922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haxe:latest`

```console
$ docker pull haxe@sha256:23122931270ff8bbe6d51e15783110ef36529f7ffcdc7169020dac96ec8846f2
```

-	Platforms:
	-	linux; amd64

### `haxe:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120566776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4402a5a14128ec81219885a5442d6fbbc5e7d710763ed406ccdb3ed4f67ce9b`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:30 GMT
ENV NEKO_VERSION=2.1.0
# Tue, 28 Feb 2017 03:25:31 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 28 Feb 2017 03:26:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "http://nekovm.org/media/neko-2.1.0-src.tar.gz" 	&& echo "0c93d5fe96240510e2d1975ae0caa9dd8eadf70d916a868684f66a099a4acf96 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 28 Feb 2017 03:29:26 GMT
ENV HAXE_VERSION=3.4.0
# Tue, 28 Feb 2017 03:30:17 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-native-compilers 		camlp4 		libxml-light-ocaml-dev 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& git clone --recursive --depth 1 --branch 3.4.0 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& make OCAMLOPT=ocamlopt.opt 	&& make install INSTALL_DIR=/usr/local 	&& cd / && haxelib setup /usr/local/lib/haxe/lib 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 28 Feb 2017 03:30:18 GMT
CMD ["haxe"]
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
	-	`sha256:7349211cd29341d185560f660c78499a748897b67eb58c08cb077843e742f2c6`  
		Last Modified: Thu, 02 Mar 2017 00:36:27 GMT  
		Size: 254.6 KB (254620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b7c094eb09fdafd36e2bf6648bd7feaa1f290daa4398625e1e1779d9892e38`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f1ae260490eff97ced26ab90532fd22598ebfc83296ab4a6c013fb920d33c3`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 2.2 MB (2191459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4eafa440bd1dec3eca7079c7aafc7963304ecb2fdddfc1beab489c3a5cb7bed`  
		Last Modified: Thu, 02 Mar 2017 00:42:45 GMT  
		Size: 5.7 MB (5719922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haxe:3.4.0-onbuild`

```console
$ docker pull haxe@sha256:58ea81c828b0fa941cb2ee5a4f66cc9b2ea1246c66e79f0007ccf046c949935b
```

-	Platforms:
	-	linux; amd64

### `haxe:3.4.0-onbuild` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120566902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09841c0973f5e909bcd329f2e14b7eb1a2470f0325ef051a9813f9195645ec93`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:30 GMT
ENV NEKO_VERSION=2.1.0
# Tue, 28 Feb 2017 03:25:31 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 28 Feb 2017 03:26:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "http://nekovm.org/media/neko-2.1.0-src.tar.gz" 	&& echo "0c93d5fe96240510e2d1975ae0caa9dd8eadf70d916a868684f66a099a4acf96 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 28 Feb 2017 03:29:26 GMT
ENV HAXE_VERSION=3.4.0
# Tue, 28 Feb 2017 03:30:17 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-native-compilers 		camlp4 		libxml-light-ocaml-dev 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& git clone --recursive --depth 1 --branch 3.4.0 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& make OCAMLOPT=ocamlopt.opt 	&& make install INSTALL_DIR=/usr/local 	&& cd / && haxelib setup /usr/local/lib/haxe/lib 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 28 Feb 2017 03:30:18 GMT
CMD ["haxe"]
# Tue, 28 Feb 2017 03:30:19 GMT
RUN mkdir -p /usr/src/app
# Tue, 28 Feb 2017 03:30:20 GMT
WORKDIR /usr/src/app
# Tue, 28 Feb 2017 03:30:20 GMT
ONBUILD COPY *.hxml /usr/src/app/
# Tue, 28 Feb 2017 03:30:20 GMT
ONBUILD RUN yes | haxelib install all
# Tue, 28 Feb 2017 03:30:21 GMT
ONBUILD COPY . /usr/src/app
# Tue, 28 Feb 2017 03:30:21 GMT
ONBUILD ARG BUILD_HXML=build.hxml
# Tue, 28 Feb 2017 03:30:21 GMT
ONBUILD RUN haxe $BUILD_HXML
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
	-	`sha256:7349211cd29341d185560f660c78499a748897b67eb58c08cb077843e742f2c6`  
		Last Modified: Thu, 02 Mar 2017 00:36:27 GMT  
		Size: 254.6 KB (254620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b7c094eb09fdafd36e2bf6648bd7feaa1f290daa4398625e1e1779d9892e38`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f1ae260490eff97ced26ab90532fd22598ebfc83296ab4a6c013fb920d33c3`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 2.2 MB (2191459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4eafa440bd1dec3eca7079c7aafc7963304ecb2fdddfc1beab489c3a5cb7bed`  
		Last Modified: Thu, 02 Mar 2017 00:42:45 GMT  
		Size: 5.7 MB (5719922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46bfad1f3ff438fd82718d6388d5367d5c2b1e8440b64ad5a02bb501217375a`  
		Last Modified: Thu, 02 Mar 2017 00:44:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haxe:3.4-onbuild`

```console
$ docker pull haxe@sha256:58ea81c828b0fa941cb2ee5a4f66cc9b2ea1246c66e79f0007ccf046c949935b
```

-	Platforms:
	-	linux; amd64

### `haxe:3.4-onbuild` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120566902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09841c0973f5e909bcd329f2e14b7eb1a2470f0325ef051a9813f9195645ec93`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Mon, 27 Feb 2017 21:14:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Mon, 27 Feb 2017 21:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 03:25:30 GMT
ENV NEKO_VERSION=2.1.0
# Tue, 28 Feb 2017 03:25:31 GMT
RUN echo 'deb http://deb.debian.org/debian jessie-backports main' > /etc/apt/sources.list.d/jessie-backports.list
# Tue, 28 Feb 2017 03:26:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "http://nekovm.org/media/neko-2.1.0-src.tar.gz" 	&& echo "0c93d5fe96240510e2d1975ae0caa9dd8eadf70d916a868684f66a099a4acf96 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 28 Feb 2017 03:29:26 GMT
ENV HAXE_VERSION=3.4.0
# Tue, 28 Feb 2017 03:30:17 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-native-compilers 		camlp4 		libxml-light-ocaml-dev 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& git clone --recursive --depth 1 --branch 3.4.0 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& make OCAMLOPT=ocamlopt.opt 	&& make install INSTALL_DIR=/usr/local 	&& cd / && haxelib setup /usr/local/lib/haxe/lib 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 28 Feb 2017 03:30:18 GMT
CMD ["haxe"]
# Tue, 28 Feb 2017 03:30:19 GMT
RUN mkdir -p /usr/src/app
# Tue, 28 Feb 2017 03:30:20 GMT
WORKDIR /usr/src/app
# Tue, 28 Feb 2017 03:30:20 GMT
ONBUILD COPY *.hxml /usr/src/app/
# Tue, 28 Feb 2017 03:30:20 GMT
ONBUILD RUN yes | haxelib install all
# Tue, 28 Feb 2017 03:30:21 GMT
ONBUILD COPY . /usr/src/app
# Tue, 28 Feb 2017 03:30:21 GMT
ONBUILD ARG BUILD_HXML=build.hxml
# Tue, 28 Feb 2017 03:30:21 GMT
ONBUILD RUN haxe $BUILD_HXML
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
	-	`sha256:7349211cd29341d185560f660c78499a748897b67eb58c08cb077843e742f2c6`  
		Last Modified: Thu, 02 Mar 2017 00:36:27 GMT  
		Size: 254.6 KB (254620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b7c094eb09fdafd36e2bf6648bd7feaa1f290daa4398625e1e1779d9892e38`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f1ae260490eff97ced26ab90532fd22598ebfc83296ab4a6c013fb920d33c3`  
		Last Modified: Thu, 02 Mar 2017 00:36:28 GMT  
		Size: 2.2 MB (2191459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4eafa440bd1dec3eca7079c7aafc7963304ecb2fdddfc1beab489c3a5cb7bed`  
		Last Modified: Thu, 02 Mar 2017 00:42:45 GMT  
		Size: 5.7 MB (5719922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46bfad1f3ff438fd82718d6388d5367d5c2b1e8440b64ad5a02bb501217375a`  
		Last Modified: Thu, 02 Mar 2017 00:44:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
