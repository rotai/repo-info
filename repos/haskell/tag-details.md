<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `haskell`

-	[`haskell:8.0.2`](#haskell802)
-	[`haskell:8.0`](#haskell80)
-	[`haskell:8`](#haskell8)
-	[`haskell:latest`](#haskelllatest)

## `haskell:8.0.2`

```console
$ docker pull haskell@sha256:c8f12dd0e017cd6d74ce0b5bd27678f11711ad4358fbfa9bdd65f34bf2ff7daa
```

-	Platforms:
	-	linux; amd64

### `haskell:8.0.2` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248862334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0487fd21eaf72cd2a944570ee8c8e126b25549ff88706613461c4f2f980f913d`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 03:24:20 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 03:25:22 GMT
RUN echo 'deb http://ppa.launchpad.net/hvr/ghc/ubuntu trusty main' > /etc/apt/sources.list.d/ghc.list &&     apt-key adv --keyserver keyserver.ubuntu.com --recv-keys F6F88286 &&     apt-get update &&     apt-get install -y --no-install-recommends cabal-install-1.24 ghc-8.0.2 happy-1.19.5 alex-3.1.7             zlib1g-dev libtinfo-dev libsqlite3-0 libsqlite3-dev ca-certificates g++ git curl &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v1.3.2/stack-1.3.2-linux-x86_64-static.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v1.3.2/stack-1.3.2-linux-x86_64-static.tar.gz.asc -o stack.tar.gz.asc &&     apt-get purge -y --auto-remove curl &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys C5705533DA4F78D8664B5DC0575159689BEFB442 &&     gpg --batch --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Feb 2017 03:25:23 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/1.24/bin:/opt/ghc/8.0.2/bin:/opt/happy/1.19.5/bin:/opt/alex/3.1.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:23 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22520ca3dbec48edd787a13dc375806985f7dd2f900b6cefa33a5593c344daf0`  
		Last Modified: Thu, 02 Mar 2017 00:34:22 GMT  
		Size: 197.5 MB (197498960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.0`

```console
$ docker pull haskell@sha256:c8f12dd0e017cd6d74ce0b5bd27678f11711ad4358fbfa9bdd65f34bf2ff7daa
```

-	Platforms:
	-	linux; amd64

### `haskell:8.0` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248862334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0487fd21eaf72cd2a944570ee8c8e126b25549ff88706613461c4f2f980f913d`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 03:24:20 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 03:25:22 GMT
RUN echo 'deb http://ppa.launchpad.net/hvr/ghc/ubuntu trusty main' > /etc/apt/sources.list.d/ghc.list &&     apt-key adv --keyserver keyserver.ubuntu.com --recv-keys F6F88286 &&     apt-get update &&     apt-get install -y --no-install-recommends cabal-install-1.24 ghc-8.0.2 happy-1.19.5 alex-3.1.7             zlib1g-dev libtinfo-dev libsqlite3-0 libsqlite3-dev ca-certificates g++ git curl &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v1.3.2/stack-1.3.2-linux-x86_64-static.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v1.3.2/stack-1.3.2-linux-x86_64-static.tar.gz.asc -o stack.tar.gz.asc &&     apt-get purge -y --auto-remove curl &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys C5705533DA4F78D8664B5DC0575159689BEFB442 &&     gpg --batch --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Feb 2017 03:25:23 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/1.24/bin:/opt/ghc/8.0.2/bin:/opt/happy/1.19.5/bin:/opt/alex/3.1.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:23 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22520ca3dbec48edd787a13dc375806985f7dd2f900b6cefa33a5593c344daf0`  
		Last Modified: Thu, 02 Mar 2017 00:34:22 GMT  
		Size: 197.5 MB (197498960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8`

```console
$ docker pull haskell@sha256:c8f12dd0e017cd6d74ce0b5bd27678f11711ad4358fbfa9bdd65f34bf2ff7daa
```

-	Platforms:
	-	linux; amd64

### `haskell:8` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248862334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0487fd21eaf72cd2a944570ee8c8e126b25549ff88706613461c4f2f980f913d`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 03:24:20 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 03:25:22 GMT
RUN echo 'deb http://ppa.launchpad.net/hvr/ghc/ubuntu trusty main' > /etc/apt/sources.list.d/ghc.list &&     apt-key adv --keyserver keyserver.ubuntu.com --recv-keys F6F88286 &&     apt-get update &&     apt-get install -y --no-install-recommends cabal-install-1.24 ghc-8.0.2 happy-1.19.5 alex-3.1.7             zlib1g-dev libtinfo-dev libsqlite3-0 libsqlite3-dev ca-certificates g++ git curl &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v1.3.2/stack-1.3.2-linux-x86_64-static.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v1.3.2/stack-1.3.2-linux-x86_64-static.tar.gz.asc -o stack.tar.gz.asc &&     apt-get purge -y --auto-remove curl &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys C5705533DA4F78D8664B5DC0575159689BEFB442 &&     gpg --batch --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Feb 2017 03:25:23 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/1.24/bin:/opt/ghc/8.0.2/bin:/opt/happy/1.19.5/bin:/opt/alex/3.1.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:23 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22520ca3dbec48edd787a13dc375806985f7dd2f900b6cefa33a5593c344daf0`  
		Last Modified: Thu, 02 Mar 2017 00:34:22 GMT  
		Size: 197.5 MB (197498960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:latest`

```console
$ docker pull haskell@sha256:c8f12dd0e017cd6d74ce0b5bd27678f11711ad4358fbfa9bdd65f34bf2ff7daa
```

-	Platforms:
	-	linux; amd64

### `haskell:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248862334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0487fd21eaf72cd2a944570ee8c8e126b25549ff88706613461c4f2f980f913d`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 03:24:20 GMT
ENV LANG=C.UTF-8
# Tue, 28 Feb 2017 03:25:22 GMT
RUN echo 'deb http://ppa.launchpad.net/hvr/ghc/ubuntu trusty main' > /etc/apt/sources.list.d/ghc.list &&     apt-key adv --keyserver keyserver.ubuntu.com --recv-keys F6F88286 &&     apt-get update &&     apt-get install -y --no-install-recommends cabal-install-1.24 ghc-8.0.2 happy-1.19.5 alex-3.1.7             zlib1g-dev libtinfo-dev libsqlite3-0 libsqlite3-dev ca-certificates g++ git curl &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v1.3.2/stack-1.3.2-linux-x86_64-static.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v1.3.2/stack-1.3.2-linux-x86_64-static.tar.gz.asc -o stack.tar.gz.asc &&     apt-get purge -y --auto-remove curl &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys C5705533DA4F78D8664B5DC0575159689BEFB442 &&     gpg --batch --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Feb 2017 03:25:23 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/1.24/bin:/opt/ghc/8.0.2/bin:/opt/happy/1.19.5/bin:/opt/alex/3.1.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Feb 2017 03:25:23 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22520ca3dbec48edd787a13dc375806985f7dd2f900b6cefa33a5593c344daf0`  
		Last Modified: Thu, 02 Mar 2017 00:34:22 GMT  
		Size: 197.5 MB (197498960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
