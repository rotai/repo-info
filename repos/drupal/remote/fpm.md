## `drupal:fpm`

```console
$ docker pull drupal@sha256:1c5c4b35439cca01cabbcf5e960373776e74247f8d1b68047bd56e105a090170
```

-	Platforms:
	-	linux; amd64

### `drupal:fpm` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168437698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f72305e084a1b1699cc1dc2fde8b850df7652c6ec10f920fd4991ba7af3508da`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 27 Feb 2017 20:34:36 GMT
ADD file:41ac8d85ee35954bf6c8353d9681a045ba260aa9a96dbbded7bcd6e37ee49bea in / 
# Mon, 27 Feb 2017 20:34:37 GMT
CMD ["/bin/bash"]
# Tue, 28 Feb 2017 17:27:47 GMT
ENV PHPIZE_DEPS=autoconf 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 28 Feb 2017 17:28:10 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		libedit2 		libsqlite3-0 		libxml2 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Tue, 28 Feb 2017 17:28:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 28 Feb 2017 17:28:12 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Tue, 28 Feb 2017 17:34:11 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Tue, 28 Feb 2017 17:34:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Tue, 28 Feb 2017 17:34:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Tue, 28 Feb 2017 17:34:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Tue, 28 Feb 2017 18:01:24 GMT
ENV GPG_KEYS=1A4E8B7277C42E53DBA9C7B9BCAA30EA9C0D5763 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Tue, 28 Feb 2017 18:01:24 GMT
ENV PHP_VERSION=7.0.16
# Tue, 28 Feb 2017 18:01:24 GMT
ENV PHP_URL=https://secure.php.net/get/php-7.0.16.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-7.0.16.tar.xz.asc/from/this/mirror
# Tue, 28 Feb 2017 18:01:24 GMT
ENV PHP_SHA256=244ac39bc657448962860aa7a590e4417f68513ad5e86ee2727b1328b0537309 PHP_MD5=6161aba9d24322d889da5d2ff944bddf
# Tue, 28 Feb 2017 18:01:33 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -r "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove $fetchDeps
# Tue, 28 Feb 2017 18:01:34 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Tue, 28 Feb 2017 18:04:58 GMT
RUN set -xe 	&& buildDeps=" 		$PHP_EXTRA_BUILD_DEPS 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 	" 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	&& docker-php-source extract 	&& cd /usr/src/php 	&& ./configure 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$PHP_EXTRA_CONFIGURE_ARGS 	&& make -j "$(nproc)" 	&& make install 	&& { find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; } 	&& make clean 	&& docker-php-source delete 		&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $buildDeps
# Tue, 28 Feb 2017 18:04:59 GMT
COPY multi:5c1cc33896847ec6f8a128a1494e83c37aea885824061e1b8e308f9e09499956 in /usr/local/bin/ 
# Tue, 28 Feb 2017 18:04:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 28 Feb 2017 18:05:00 GMT
WORKDIR /var/www/html
# Tue, 28 Feb 2017 18:05:01 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = [::]:9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 28 Feb 2017 18:05:01 GMT
EXPOSE 9000/tcp
# Tue, 28 Feb 2017 18:05:01 GMT
CMD ["php-fpm"]
# Wed, 01 Mar 2017 23:47:42 GMT
RUN set -ex 	&& buildDeps=' 		libjpeg62-turbo-dev 		libpng12-dev 		libpq-dev 	' 	&& apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd 		--with-jpeg-dir=/usr 		--with-png-dir=/usr 	&& docker-php-ext-install -j "$(nproc)" gd mbstring opcache pdo pdo_mysql pdo_pgsql zip 	&& apt-mark manual 		libjpeg62-turbo 		libpq5 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 01 Mar 2017 23:47:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 		echo 'opcache.enable_cli=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 01 Mar 2017 23:47:43 GMT
WORKDIR /var/www/html
# Wed, 01 Mar 2017 23:47:44 GMT
ENV DRUPAL_VERSION=8.2.6
# Wed, 01 Mar 2017 23:47:44 GMT
ENV DRUPAL_MD5=57526a827771ea8a06db1792f1602a85
# Wed, 01 Mar 2017 23:47:51 GMT
RUN curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz 	&& echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f drupal.tar.gz 	&& rm drupal.tar.gz 	&& chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:693502eb7dfbc6b94964ae66ebc72d3e32facd981c72995b09794f1e87bac184`  
		Last Modified: Mon, 27 Feb 2017 20:40:26 GMT  
		Size: 51.4 MB (51363374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16328c296404224e6ea0407465417f60cbc7695e30c96cc8c334fa9760d454db`  
		Last Modified: Wed, 01 Mar 2017 16:51:36 GMT  
		Size: 77.6 MB (77607519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3c97761df63da7ca7ba549d5ad5f3011ae08e34bb95487537b5431229665db`  
		Last Modified: Wed, 01 Mar 2017 16:51:10 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cc94ef9aa275aff6912d0a832f373fdf1d02f65d85c27631da030f78c3f3c3`  
		Last Modified: Wed, 01 Mar 2017 17:04:04 GMT  
		Size: 12.7 MB (12698398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c4e4d1b4930af6154f6f3756aa7f6303e515a11753cb4b47c1cba0c65a7b46`  
		Last Modified: Wed, 01 Mar 2017 17:04:01 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e0c6e34d02c11003900e974f57d1f27ddf53a068a0bb703b0fa900d57fbdda`  
		Last Modified: Wed, 01 Mar 2017 17:04:07 GMT  
		Size: 12.8 MB (12843321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e76d885b0840b8a1fad55095d08a5a624faa554ebc2c883b0be61a557f5983`  
		Last Modified: Wed, 01 Mar 2017 17:04:01 GMT  
		Size: 2.0 KB (2013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513bff7955a730257370ada9380e0a9f4b3d160d0cd519ae512e633f3e94cf57`  
		Last Modified: Wed, 01 Mar 2017 17:04:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890323f3a3b09e471844df22d3dda2f52ef86beed4932647a69f3ca1002dcc9d`  
		Last Modified: Wed, 01 Mar 2017 17:04:01 GMT  
		Size: 7.7 KB (7687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdcae9505505b802515f7ef1b3e93048c8ce5467aa84084070acf778781949f`  
		Last Modified: Thu, 02 Mar 2017 00:01:20 GMT  
		Size: 1.7 MB (1735005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b65e783c06b3d20ad958541c40c8a40f7a7792399d26094a1c34a1c2c110233`  
		Last Modified: Thu, 02 Mar 2017 00:01:19 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f79b06bdc783a85676a2d5a2443f8fca420f94fc65d93dadc34d16501b7c01a`  
		Last Modified: Thu, 02 Mar 2017 00:01:35 GMT  
		Size: 12.2 MB (12179249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
