## `traefik:camembert-alpine`

```console
$ docker pull traefik@sha256:57678d0df9f48fa1e186d489c2c35c845abf409be864ca7830b5e2783da1b81a
```

-	Platforms:
	-	linux; amd64

### `traefik:camembert-alpine` - linux; amd64

-	Docker Version: 1.12.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8974034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57789a5996f02e91019f2a5de941514b24d0e4858cda22334d0661deb9fe2ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["--help"]`

```dockerfile
# Tue, 18 Oct 2016 20:31:22 GMT
ADD file:7afbc23fda8b0b3872623c16af8e3490b2cee951aed14b3794389c2f946cc8c7 in / 
# Mon, 21 Nov 2016 17:43:51 GMT
RUN apk --update upgrade     && apk --no-cache --no-progress add ca-certificates     && rm -rf /var/cache/apk/*
# Mon, 21 Nov 2016 17:43:52 GMT
COPY file:9d45e32877bd64a9d44d780c7648e40cdf997f2bb63b43c12af0eeb8f4a42c7c in /usr/local/bin/ 
# Mon, 21 Nov 2016 17:43:52 GMT
COPY file:41f5bd1ea0a61e819b7d8c5489c305d4f2798046917dd6b6695318f555981727 in / 
# Mon, 21 Nov 2016 17:43:53 GMT
EXPOSE 80/tcp
# Mon, 21 Nov 2016 17:43:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 21 Nov 2016 17:43:54 GMT
CMD ["--help"]
# Mon, 21 Nov 2016 17:43:54 GMT
LABEL org.label-schema.vendor=Containous org.label-schema.url=https://traefik.io org.label-schema.name=Traefik org.label-schema.description=A modern reverse-proxy org.label-schema.version=v1.1.0 org.label-schema.docker.schema-version=1.0
```

-	Layers:
	-	`sha256:3690ec4760f95690944da86dc4496148a63d85c9e3100669a318110092f6862f`  
		Last Modified: Tue, 18 Oct 2016 20:32:39 GMT  
		Size: 2.3 MB (2312958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d5cfd5b8a3036de2e1fcd7d02dda0290defd69d9248b43e53932852cc1083c`  
		Last Modified: Mon, 21 Nov 2016 17:44:54 GMT  
		Size: 1.2 MB (1206402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ac6972780eae0c564349b2cdca2fa2416a3ea5e5dab393e11abccf556e5629`  
		Last Modified: Mon, 21 Nov 2016 17:44:57 GMT  
		Size: 5.5 MB (5454333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3394f99c1106bca9fc9a7996ea1b0cdd429525a9e21cfae16699713cd424ac9f`  
		Last Modified: Mon, 21 Nov 2016 17:44:54 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip