<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `r-base`

-	[`r-base:3.3.2`](#r-base332)
-	[`r-base:latest`](#r-baselatest)

## `r-base:3.3.2`

```console
$ docker pull r-base@sha256:f3cca3cadda5451f0399b83484454ed46bd2712784f83f6515adbeac7ee240af
```

-	Platforms:
	-	linux; amd64

### `r-base:3.3.2` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259701080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38270dc4745b49a29f8e0f793449b3845db7d3479e349b44c5b398012b5c9a8a`
-	Default Command: `["R"]`

```dockerfile
# Mon, 27 Feb 2017 20:38:04 GMT
ADD file:01254ecc543a99dbce9f9b5110d2445fcf0e14056845bdc15d992a424f150518 in / 
# Mon, 27 Feb 2017 20:38:05 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 22:38:50 GMT
MAINTAINER "Carl Boettiger and Dirk Eddelbuettel" rocker-maintainers@eddelbuettel.com
# Tue, 28 Feb 2017 22:38:52 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 28 Feb 2017 22:39:11 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:39:13 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 28 Feb 2017 22:39:13 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 28 Feb 2017 22:39:13 GMT
ENV LANG=en_US.UTF-8
# Tue, 28 Feb 2017 22:39:14 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list 	&& echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Tue, 28 Feb 2017 22:39:15 GMT
ENV R_BASE_VERSION=3.3.2
# Tue, 28 Feb 2017 22:41:04 GMT
RUN apt-get update 	&& apt-get install -t unstable -y --no-install-recommends 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}* 		r-base-dev=${R_BASE_VERSION}* 		r-recommended=${R_BASE_VERSION}*         && echo 'options(repos = c(CRAN = "https://cran.rstudio.com/"), download.file.method = "libcurl")' >> /etc/R/Rprofile.site         && echo 'source("/etc/R/Rprofile.site")' >> /etc/littler.r 	&& ln -s /usr/share/doc/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/share/doc/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/share/doc/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/share/doc/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:41:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:89e43290682b07840695ec8e1d171055799d900895f012f5bcd10e4d87adb86e`  
		Last Modified: Mon, 27 Feb 2017 20:48:15 GMT  
		Size: 44.1 MB (44066758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448f13e41980efb068c4fb939ab00abb10b293dfec8dbb8353711d83946adb15`  
		Last Modified: Thu, 02 Mar 2017 03:31:34 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b2d56b2653b7f7658fd8cbee4092fec04dd5a6ad822cfcb170fe046a3940b7`  
		Last Modified: Thu, 02 Mar 2017 03:31:46 GMT  
		Size: 35.8 MB (35776303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a555c31a0358f10ef0e69eb540fed87089236b418e884bfc58aebdcf75a32`  
		Last Modified: Thu, 02 Mar 2017 03:31:34 GMT  
		Size: 341.0 KB (340956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7157248b9dbe7752b6b07f7cc63dd83a72e88192a37d88a58b61b540cb4d0ff`  
		Last Modified: Thu, 02 Mar 2017 03:31:34 GMT  
		Size: 291.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503486b6996de02d9ff09950acbeab9afb3ad35d79533b06e400de519550c28f`  
		Last Modified: Thu, 02 Mar 2017 03:32:22 GMT  
		Size: 179.5 MB (179514953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `r-base:latest`

```console
$ docker pull r-base@sha256:f3cca3cadda5451f0399b83484454ed46bd2712784f83f6515adbeac7ee240af
```

-	Platforms:
	-	linux; amd64

### `r-base:latest` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259701080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38270dc4745b49a29f8e0f793449b3845db7d3479e349b44c5b398012b5c9a8a`
-	Default Command: `["R"]`

```dockerfile
# Mon, 27 Feb 2017 20:38:04 GMT
ADD file:01254ecc543a99dbce9f9b5110d2445fcf0e14056845bdc15d992a424f150518 in / 
# Mon, 27 Feb 2017 20:38:05 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 22:38:50 GMT
MAINTAINER "Carl Boettiger and Dirk Eddelbuettel" rocker-maintainers@eddelbuettel.com
# Tue, 28 Feb 2017 22:38:52 GMT
RUN useradd docker 	&& mkdir /home/docker 	&& chown docker:docker /home/docker 	&& addgroup docker staff
# Tue, 28 Feb 2017 22:39:11 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		ed 		less 		locales 		vim-tiny 		wget 		ca-certificates 		fonts-texgyre 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:39:13 GMT
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen 	&& locale-gen en_US.utf8 	&& /usr/sbin/update-locale LANG=en_US.UTF-8
# Tue, 28 Feb 2017 22:39:13 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 28 Feb 2017 22:39:13 GMT
ENV LANG=en_US.UTF-8
# Tue, 28 Feb 2017 22:39:14 GMT
RUN echo "deb http://http.debian.net/debian sid main" > /etc/apt/sources.list.d/debian-unstable.list 	&& echo 'APT::Default-Release "testing";' > /etc/apt/apt.conf.d/default
# Tue, 28 Feb 2017 22:39:15 GMT
ENV R_BASE_VERSION=3.3.2
# Tue, 28 Feb 2017 22:41:04 GMT
RUN apt-get update 	&& apt-get install -t unstable -y --no-install-recommends 		littler                 r-cran-littler 		r-base=${R_BASE_VERSION}* 		r-base-dev=${R_BASE_VERSION}* 		r-recommended=${R_BASE_VERSION}*         && echo 'options(repos = c(CRAN = "https://cran.rstudio.com/"), download.file.method = "libcurl")' >> /etc/R/Rprofile.site         && echo 'source("/etc/R/Rprofile.site")' >> /etc/littler.r 	&& ln -s /usr/share/doc/littler/examples/install.r /usr/local/bin/install.r 	&& ln -s /usr/share/doc/littler/examples/install2.r /usr/local/bin/install2.r 	&& ln -s /usr/share/doc/littler/examples/installGithub.r /usr/local/bin/installGithub.r 	&& ln -s /usr/share/doc/littler/examples/testInstalled.r /usr/local/bin/testInstalled.r 	&& install.r docopt 	&& rm -rf /tmp/downloaded_packages/ /tmp/*.rds 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Feb 2017 22:41:05 GMT
CMD ["R"]
```

-	Layers:
	-	`sha256:89e43290682b07840695ec8e1d171055799d900895f012f5bcd10e4d87adb86e`  
		Last Modified: Mon, 27 Feb 2017 20:48:15 GMT  
		Size: 44.1 MB (44066758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448f13e41980efb068c4fb939ab00abb10b293dfec8dbb8353711d83946adb15`  
		Last Modified: Thu, 02 Mar 2017 03:31:34 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b2d56b2653b7f7658fd8cbee4092fec04dd5a6ad822cfcb170fe046a3940b7`  
		Last Modified: Thu, 02 Mar 2017 03:31:46 GMT  
		Size: 35.8 MB (35776303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0a555c31a0358f10ef0e69eb540fed87089236b418e884bfc58aebdcf75a32`  
		Last Modified: Thu, 02 Mar 2017 03:31:34 GMT  
		Size: 341.0 KB (340956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7157248b9dbe7752b6b07f7cc63dd83a72e88192a37d88a58b61b540cb4d0ff`  
		Last Modified: Thu, 02 Mar 2017 03:31:34 GMT  
		Size: 291.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503486b6996de02d9ff09950acbeab9afb3ad35d79533b06e400de519550c28f`  
		Last Modified: Thu, 02 Mar 2017 03:32:22 GMT  
		Size: 179.5 MB (179514953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
