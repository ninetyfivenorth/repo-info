## `buildpack-deps:artful`

```console
$ docker pull buildpack-deps@sha256:4bdf8e2449438312b1acbd98252cd021144cd7cce40f3083759f494770542482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:artful` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:693e21bc388d076eb48b681e884019ae2e2849d0208d57cd5920cf813fe53a21
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (262996472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125aa125d52e3108065ed7e89964cd4a0d900cffe9a9a9147c0c237e8d338f28`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 27 Apr 2018 23:27:44 GMT
ADD file:df6f43debb851b500998be63726b49b8c538d7774e4b83a0dedba70e4b9deebc in / 
# Fri, 27 Apr 2018 23:27:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 27 Apr 2018 23:27:45 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 27 Apr 2018 23:27:46 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Fri, 27 Apr 2018 23:27:47 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 27 Apr 2018 23:27:48 GMT
CMD ["/bin/bash"]
# Sat, 28 Apr 2018 15:04:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 15:04:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 15:06:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 15:10:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:68393378db126aa9d5d472dedd01f35de1ae7eb7bafa4647fc872d53dfdb36d0`  
		Last Modified: Thu, 19 Apr 2018 21:05:43 GMT  
		Size: 40.5 MB (40542165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3366501e0e91c5d678aede5407db895b70acce87328b6ffd66ba758526d183`  
		Last Modified: Fri, 27 Apr 2018 23:30:52 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156ec05da9a5ef7eacc75baed16b2d9c4d3ccc7e25a1996d80f163a36b143884`  
		Last Modified: Fri, 27 Apr 2018 23:30:51 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281cba1133d9a42cfc3ca0b2ac71d7a9905f47eb3351de164b58ca2f0a861c96`  
		Last Modified: Fri, 27 Apr 2018 23:30:51 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acdc2cc8ed1096fd67668440cbebf09aad3490428e7d9a9b618ea29ead27547`  
		Last Modified: Fri, 27 Apr 2018 23:30:51 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05eb28739dafb0cedf925286a5b3ea697cfefef214d16822140a2956bd447ff`  
		Last Modified: Sat, 28 Apr 2018 18:59:16 GMT  
		Size: 6.1 MB (6055323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33dc5348860c007a5ac5ffd8a9fb822895abb820f75f38760bb2e90ac6b7cc5`  
		Last Modified: Sat, 28 Apr 2018 19:02:16 GMT  
		Size: 45.7 MB (45741222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d321f2534132e90e1633775142f8dfc9cb9ddd4d8951d523a9b97d3b8d5c6c`  
		Last Modified: Sat, 28 Apr 2018 19:08:48 GMT  
		Size: 170.7 MB (170655289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:artful` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e9f1943c064c0baa9d86e3cc00ffb3514003298c2ff9249b40c6ec61ea9f9f9f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233683512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd008d9f6fa1fc50985155f44c322cd3acbb4e837bc7e4fa06b486ff2fd4026`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Apr 2018 12:03:14 GMT
ADD file:a333e18e1717a1b7a9d4595ac663cebae53e262e9ada3b000c6dbda4c078a2be in / 
# Sat, 28 Apr 2018 12:03:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 28 Apr 2018 12:03:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 12:03:19 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Sat, 28 Apr 2018 12:03:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 28 Apr 2018 12:03:26 GMT
CMD ["/bin/bash"]
# Sat, 28 Apr 2018 12:26:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 12:26:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 12:27:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 12:29:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6d9fb8e5706c9e84d87c41776e65b245a29a54bd580aba8b6829415ddf511093`  
		Last Modified: Sat, 28 Apr 2018 12:06:16 GMT  
		Size: 36.1 MB (36094951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e55c7c1ad2064c99e7bbe5f1b8cbf0ded890015f2a4ae620e492a0efb99234`  
		Last Modified: Sat, 28 Apr 2018 12:06:08 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4401b2302372bd5dde97dd509dd12d4c458249c2f109318fa2009ff5fa06321a`  
		Last Modified: Sat, 28 Apr 2018 12:06:06 GMT  
		Size: 610.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86bd15ca9cc5ce102c8933200611f51ab428c021147e5703126c0116ce25124`  
		Last Modified: Sat, 28 Apr 2018 12:06:06 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7aadd8fcbc4237677a2a7b40fd22d3cc7384ce852856d50ee36f055dadeb032`  
		Last Modified: Sat, 28 Apr 2018 12:06:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c1640c47a99436814b677e12d96c4bbacfa3d539cb8a4b00a1b2d2527405d9`  
		Last Modified: Sat, 28 Apr 2018 12:57:04 GMT  
		Size: 5.1 MB (5097547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebef9fe80f248d7cde01191108351294d3002b8fba545b8d375405af2509ba2e`  
		Last Modified: Sat, 28 Apr 2018 12:57:41 GMT  
		Size: 41.9 MB (41852548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf379fd34ff13614fddec4b6ae7a330105407f0584e439d8cdb5a277c1a44618`  
		Last Modified: Sat, 28 Apr 2018 12:58:40 GMT  
		Size: 150.6 MB (150635968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:artful` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:15b642207fc9da2d06d3d383d196a7e51341fd5813d44574ed6965e677ba7ac3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247160407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40fca392fe13c0142bac4b0f49b320add2280fec0820e7c911e83bbd1bf9fc22`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 May 2018 01:09:19 GMT
ADD file:748eee72f4e00f2d01e9ee4a08ee8c4e95fe5a51b8be551df98341e9cab52511 in / 
# Tue, 01 May 2018 01:09:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 01 May 2018 01:09:28 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 01 May 2018 01:09:32 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Tue, 01 May 2018 01:09:41 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 01 May 2018 01:09:54 GMT
CMD ["/bin/bash"]
# Tue, 01 May 2018 06:57:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 May 2018 06:57:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 May 2018 06:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 May 2018 07:09:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5b0e0be5a93e4aed8fd8714a22af66b85f62d0fbeaa6ea8786e3fff1d560581a`  
		Last Modified: Mon, 23 Apr 2018 14:48:19 GMT  
		Size: 37.4 MB (37413889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4ae9146c7d93ba07db364c9d3731b91c5ac3b24e0b035a039336c787ba9ea7`  
		Last Modified: Tue, 01 May 2018 01:14:08 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525ae34bdfbda6761f6b495ee5604e2e51e10776024c79600308ab67e5fceb12`  
		Last Modified: Tue, 01 May 2018 01:14:08 GMT  
		Size: 536.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e1211a9e40602b93646e57414c17a484788297510700821094aed4130af786`  
		Last Modified: Tue, 01 May 2018 01:14:08 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489f3a180b16620ce4d491a2d75d7954fe07b6c79e1c92a1ea43ebb37e2476d4`  
		Last Modified: Tue, 01 May 2018 01:14:08 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c563056c40ef93adcd204787bdeb185331b31e1a5cf361d03aa8099218147798`  
		Last Modified: Tue, 01 May 2018 08:44:52 GMT  
		Size: 5.3 MB (5334356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a877125f3ee72a1ed78a59037ac761a395e2cecc3cfb003b05f21af3dbe43668`  
		Last Modified: Tue, 01 May 2018 08:45:45 GMT  
		Size: 44.0 MB (43964966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50e1af6739ec7367adaa28f4e44b8505b4b5e4e359ac3acf217f90990488c68`  
		Last Modified: Tue, 01 May 2018 08:48:00 GMT  
		Size: 160.4 MB (160444790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:artful` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0a3582d8929e40b97787e90ac210d2065d36b9a22aacf74607f24aad5aab62dd
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265347825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea69c899e258c16bd8d99f5d5d16ebb6afdb87889b0fefb8b18178f63920ab2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Apr 2018 11:17:38 GMT
ADD file:669d953dcffd48718fa9552ac17fa437c4f7808c809d4dca3a985fbd92e44d9d in / 
# Sat, 28 Apr 2018 11:17:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 28 Apr 2018 11:17:39 GMT
RUN rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 11:17:40 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Sat, 28 Apr 2018 11:17:40 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 28 Apr 2018 11:17:41 GMT
CMD ["/bin/bash"]
# Sat, 28 Apr 2018 11:48:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 11:48:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 11:49:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 11:53:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b38f2cab2cd1e5a5828e843f9949b681b1d0c7fb6067f45e0bd32ce5b2a0271a`  
		Last Modified: Mon, 23 Apr 2018 14:47:49 GMT  
		Size: 41.3 MB (41342461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164a6406f7a5ac124c49d20db841afe41c9168abeb5f46130898381ca955ad67`  
		Last Modified: Sat, 28 Apr 2018 11:18:39 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4327f33595f48e0c323bf66942a812fff4ccedbb316aa2d499819b1edd3fb8ad`  
		Last Modified: Sat, 28 Apr 2018 11:18:39 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12f041d77d086bf7a1ae9c1fe78de3f4da87ff376f3ce89328c50a4604552c4`  
		Last Modified: Sat, 28 Apr 2018 11:18:39 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10dce514c02c5a0db8bc64fe9ae603660dc482ea4300cb075875946d048713e2`  
		Last Modified: Sat, 28 Apr 2018 11:18:39 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca5979ab452604aca47a725ed14d7d565235f573078c395ba61587543a8ef1f`  
		Last Modified: Sat, 28 Apr 2018 12:30:54 GMT  
		Size: 6.1 MB (6109011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4888b9737ba90c455a7964c55191d0b53d5eaf8954ea7c4f86546782d044f8`  
		Last Modified: Sat, 28 Apr 2018 12:31:24 GMT  
		Size: 47.3 MB (47346048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af545dd5398d8df98835d038f3f3c0a1dde290d45db454eac434763c85ae4095`  
		Last Modified: Sat, 28 Apr 2018 12:32:30 GMT  
		Size: 170.5 MB (170547874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:artful` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:381566a0e5132cb45e08466c778f4408ff1ffcd1f9d38aa54f269142cf8f6080
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283942115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc631e68fd42fca73df7aa523ca850b7a589ea936f6e81cbcef1b96bf4d79db`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Apr 2018 08:34:17 GMT
ADD file:fbd8bf2e9e4258327659b9bf92ea09881deba085dfc47bcd6c9c0e3ab6f5e055 in / 
# Sat, 28 Apr 2018 08:34:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 28 Apr 2018 08:34:21 GMT
RUN rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 08:34:23 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Sat, 28 Apr 2018 08:34:24 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 28 Apr 2018 08:34:25 GMT
CMD ["/bin/bash"]
# Sat, 28 Apr 2018 09:31:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 09:31:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 09:32:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 09:38:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b4f561f7b9d5dc7d90dfe9f3035cfac27da95f9d7f6cb4c66f6d3c2a20b51300`  
		Last Modified: Sat, 28 Apr 2018 08:36:18 GMT  
		Size: 43.8 MB (43778479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4e67575e5620e4a2469081b3c31793774c12197d559beccb2096c8b4008c84`  
		Last Modified: Sat, 28 Apr 2018 08:36:07 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962df9b88884a533546e0bc02f9da5630142a6da1ec82ddc8e99b58b4c1f0be0`  
		Last Modified: Sat, 28 Apr 2018 08:36:07 GMT  
		Size: 578.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9274c171c2d6db20f9d1b41920f2a635886769f472fb1b02f75d7f3245f30336`  
		Last Modified: Sat, 28 Apr 2018 08:36:07 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d5e18a9f5a85a15746868e34cad0a15b63a3087883b198471a151a5feb69f3`  
		Last Modified: Sat, 28 Apr 2018 08:36:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7ecfa2fef6b03c03e41a875a2f497e3e2d7a9d3ee93cd1486aeb81569e6b9b`  
		Last Modified: Sat, 28 Apr 2018 10:31:46 GMT  
		Size: 6.1 MB (6135944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b7c419d01256084941df5d65c20164bccc5b27bad17209dfbe5f5daed73333`  
		Last Modified: Sat, 28 Apr 2018 10:32:25 GMT  
		Size: 53.3 MB (53297034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e581a45195dff48af89ec9e25b1a9e19186c717eb711da11c6d3de270617fff3`  
		Last Modified: Sat, 28 Apr 2018 10:33:55 GMT  
		Size: 180.7 MB (180728191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:artful` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d77310beaa8feedbd5c383fbe6504ef7cb8a75b1ef9c7ec9f5adba218ba5a792
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248707014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bae7a924d1065c92bfa8ac7dc3d07146104279cfdfb3e8d3c2b2ab29a0a894b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 28 Apr 2018 11:54:25 GMT
ADD file:cb7f19b06f953d1330a7fbd425bf6fa2c1003d4849701eb98973bce8e22aaf81 in / 
# Sat, 28 Apr 2018 11:54:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 28 Apr 2018 11:54:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 11:54:27 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Sat, 28 Apr 2018 11:54:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 28 Apr 2018 11:54:28 GMT
CMD ["/bin/bash"]
# Sat, 28 Apr 2018 13:02:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 13:02:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 13:03:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 13:05:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:acab74b0235bba0be1794a08b59897aa2d71f537c50ab400021216437029b738`  
		Last Modified: Thu, 26 Apr 2018 14:27:48 GMT  
		Size: 39.2 MB (39176846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f567b6a1ffc1b337f6563b4611f040e483de6293c1a61b39de02b7ded807e0`  
		Last Modified: Sat, 28 Apr 2018 11:55:19 GMT  
		Size: 837.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e6c67620a1f65a59570a0c4e31e8bc0d03516560c98c949382a01ed9a4f77b`  
		Last Modified: Sat, 28 Apr 2018 11:55:19 GMT  
		Size: 537.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918cd43a954a71aa39c756394e83d5a9dda1f12a2ab3779e938235c88cf96af8`  
		Last Modified: Sat, 28 Apr 2018 11:55:19 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e90df47bed7423f2af475e32fc5c690138ffea48f88d8a5140991eaab2b8a6`  
		Last Modified: Sat, 28 Apr 2018 11:55:19 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d467153fd0aa4dd503a0c493262cbb9a81d78ac3eda319d5d8ae71811f4989`  
		Last Modified: Sat, 28 Apr 2018 13:25:00 GMT  
		Size: 5.7 MB (5741272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c845ccf11d1af92b17934803d827a58297b33803ef32017ff426f05fe16d49c`  
		Last Modified: Sat, 28 Apr 2018 13:25:26 GMT  
		Size: 45.7 MB (45677709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c87a8de7fa3836fffe5efc735ca6f8dc7239e18a280b5cd01881b930f2e3edc`  
		Last Modified: Sat, 28 Apr 2018 13:26:12 GMT  
		Size: 158.1 MB (158108800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
