## `influxdb:meta-alpine`

```console
$ docker pull influxdb@sha256:e120e51363d6797297b4b8c7d35d15bbff06c12bb212340bfd6bf11ad11b9d06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:meta-alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:c0ef68e3cd2c8f1b6740e1345c46149a634e6c453ad2448bc51975ca32a2b7e2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221e76fe77781bee7de4e810c2ebbd97ef7246f9eac212d27d5b1173b40625af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd-meta"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:38 GMT
ADD file:6edc55fb54ec9fc3658c8f5176a70e792103a516154442f94fed8e0290e4960e in / 
# Tue, 09 Jan 2018 21:10:38 GMT
CMD ["/bin/sh"]
# Tue, 09 Jan 2018 21:31:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 13 Jan 2018 01:39:13 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Sat, 14 Apr 2018 04:04:39 GMT
ENV INFLUXDB_VERSION=1.5.2-c1.5.2
# Sat, 14 Apr 2018 04:12:57 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/enterprise/releases/influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-meta-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb-meta.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 14 Apr 2018 04:12:57 GMT
COPY file:95a6fe33e203909c093135fff9ff2b4cdc02ca4f1fe1dec109b5a9cf6b7a0946 in /etc/influxdb/influxdb-meta.conf 
# Sat, 14 Apr 2018 04:12:58 GMT
EXPOSE 8091/tcp
# Sat, 14 Apr 2018 04:12:58 GMT
VOLUME [/var/lib/influxdb]
# Sat, 14 Apr 2018 04:12:59 GMT
COPY file:b4fa000cf2aff5bf4e5093021ca6255fffa17c43ae18eb4c55ae28a3cc2dc281 in /entrypoint.sh 
# Sat, 14 Apr 2018 04:12:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 14 Apr 2018 04:12:59 GMT
CMD ["influxd-meta"]
```

-	Layers:
	-	`sha256:605ce1bd3f3164f2949a30501cc596f52a72de05da1306ab360055f0d7130c32`  
		Last Modified: Tue, 09 Jan 2018 21:13:17 GMT  
		Size: 2.0 MB (1991747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfc8b91e98122366108d51bd0925304ee67ee4ec9ac28b15a1d3374e5fed982`  
		Last Modified: Tue, 09 Jan 2018 21:32:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b6c161ff2e67675f87132cc71e97fb00eb631fda65f42bb1f42e0a4597c178`  
		Last Modified: Sat, 13 Jan 2018 01:41:17 GMT  
		Size: 1.8 MB (1848579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b370ef77c198b3f25bcffbbf270593893e1a8d75a6fe6ee126e1656a48dd1f9`  
		Last Modified: Sat, 14 Apr 2018 05:53:09 GMT  
		Size: 11.2 MB (11150506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b88c9a2dfe5b9ef01485727d8815c3b468e7bfb2a657ccc244fb2b7e67c9cd7`  
		Last Modified: Sat, 14 Apr 2018 05:53:06 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2782d1fa437a0e75a522b005d0fa5df10579d5f50a9369aa40946423b9b0bb58`  
		Last Modified: Sat, 14 Apr 2018 05:53:06 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
