## `node:9-onbuild`

```console
$ docker pull node@sha256:0060d3155cf9eac3c144696f5bd4f9d9419e8997825e7e2d1a76b0374908a3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `node:9-onbuild` - linux; amd64

```console
$ docker pull node@sha256:cc2f2ac3642b1ae4927c8e6004008cf9e817e266f402e5a34dcce403a780444d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 MB (265885120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a905d4fe58afdce2499916fc40f47aa6c811671b662bcb52f7448bf14636815`
-	Default Command: `["npm","start"]`

```dockerfile
# Sat, 28 Apr 2018 06:44:15 GMT
ADD file:3e6141c0c9cb74b14a281eb3ab7aaf162a625733e652c3948b323bb2ec8b4343 in / 
# Sat, 28 Apr 2018 06:44:16 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 16:12:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 16:12:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 16:22:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 16:24:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 May 2018 22:14:46 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 02 May 2018 22:14:51 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Wed, 02 May 2018 22:14:52 GMT
ENV NODE_VERSION=9.11.1
# Wed, 02 May 2018 22:15:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 02 May 2018 22:15:00 GMT
ENV YARN_VERSION=1.5.1
# Wed, 02 May 2018 22:15:05 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Wed, 02 May 2018 22:15:06 GMT
CMD ["node"]
# Wed, 02 May 2018 22:15:31 GMT
RUN mkdir -p /usr/src/app
# Wed, 02 May 2018 22:15:31 GMT
WORKDIR /usr/src/app
# Wed, 02 May 2018 22:15:32 GMT
ONBUILD ARG NODE_ENV
# Wed, 02 May 2018 22:15:32 GMT
ONBUILD ENV NODE_ENV $NODE_ENV
# Wed, 02 May 2018 22:15:32 GMT
ONBUILD COPY package.json /usr/src/app/
# Wed, 02 May 2018 22:15:33 GMT
ONBUILD RUN npm install && npm cache clean --force
# Wed, 02 May 2018 22:15:33 GMT
ONBUILD COPY . /usr/src/app
# Wed, 02 May 2018 22:15:33 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:3d77ce4481b119f00e53bee9b4a443469c42c224db954ddaa2e6b74cd73cd5d0`  
		Last Modified: Sat, 28 Apr 2018 08:24:47 GMT  
		Size: 54.3 MB (54262566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d9ca1153eba1cbf763dbc8fc4cbb886420e713077c1d125c684605e239828a`  
		Last Modified: Sat, 28 Apr 2018 20:23:15 GMT  
		Size: 17.6 MB (17564359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d024d87fd1575e704886f4e70af4ece1d2d9c757f61f27e2af4488c228b0b41`  
		Last Modified: Sat, 28 Apr 2018 20:24:13 GMT  
		Size: 43.3 MB (43253845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a13018a3aff59008b3f3c97087e6ea1511ef033b98deec2e4b2704afa85fe6`  
		Last Modified: Sat, 28 Apr 2018 20:25:27 GMT  
		Size: 131.1 MB (131069905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0a45c8d5abdeedff89299a124e0256f9ac27d9d7af283aa3bd83ab629de075`  
		Last Modified: Wed, 02 May 2018 22:42:46 GMT  
		Size: 4.4 KB (4426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fb6314ce8c057122c370a4bfd72328797aaf752432d2495d09f4ab6e806243`  
		Last Modified: Wed, 02 May 2018 22:42:46 GMT  
		Size: 117.6 KB (117625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f12d719065d44eb3d8024767d48e4c98df6bc9f6649ff535d0f13106e71c369`  
		Last Modified: Wed, 02 May 2018 22:42:52 GMT  
		Size: 18.6 MB (18551240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c2e29bfe54172b76ee09ce9ce6e254f9b17d8b65dbe4d7bb5ca3bf760b9524`  
		Last Modified: Wed, 02 May 2018 22:42:46 GMT  
		Size: 1.1 MB (1061023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03822da90acedff5866b4a9c446636da09a69d6ad6f4395100264a9230523f98`  
		Last Modified: Wed, 02 May 2018 22:56:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:9-onbuild` - linux; arm variant v7

```console
$ docker pull node@sha256:d605492125cadafd8db89db9c14c5b2f67246c395d295b047055b1a6e9698d28
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.6 MB (239619005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981dedc0941e9fab5bef866043871d8c5c2b665f6c4dff173c1b69121854962f`
-	Default Command: `["npm","start"]`

```dockerfile
# Sat, 28 Apr 2018 11:59:05 GMT
ADD file:4e9c283075c120ce66f83bf541b0aeaa8a46f74c21d38e4ab1578e7f1b892823 in / 
# Sat, 28 Apr 2018 11:59:05 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 12:36:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 12:36:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 12:37:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 12:39:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 15:42:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 15:42:18 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 15:42:18 GMT
ENV NODE_VERSION=9.11.1
# Sat, 28 Apr 2018 15:42:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 15:42:25 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 15:42:27 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 15:42:27 GMT
CMD ["node"]
# Sat, 28 Apr 2018 15:42:47 GMT
RUN mkdir -p /usr/src/app
# Sat, 28 Apr 2018 15:42:47 GMT
WORKDIR /usr/src/app
# Sat, 28 Apr 2018 15:42:47 GMT
ONBUILD ARG NODE_ENV
# Sat, 28 Apr 2018 15:42:48 GMT
ONBUILD ENV NODE_ENV $NODE_ENV
# Sat, 28 Apr 2018 15:42:48 GMT
ONBUILD COPY package.json /usr/src/app/
# Sat, 28 Apr 2018 15:42:48 GMT
ONBUILD RUN npm install && npm cache clean --force
# Sat, 28 Apr 2018 15:42:49 GMT
ONBUILD COPY . /usr/src/app
# Sat, 28 Apr 2018 15:42:49 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:5c478157e28e3c26a0209484edb518799e1c21863d4700579c010b7203e0537f`  
		Last Modified: Sat, 28 Apr 2018 12:10:24 GMT  
		Size: 50.2 MB (50195697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8594897c8bf4818e6046e6e628a380bf5e4460a7bbd5db964170e47643d78fcc`  
		Last Modified: Sat, 28 Apr 2018 13:03:02 GMT  
		Size: 16.7 MB (16738795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a8d9b47a39f0c687594e30f9584bb58074510ab097a17f8f852f16da395908`  
		Last Modified: Sat, 28 Apr 2018 13:03:27 GMT  
		Size: 39.7 MB (39727093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127ed1c030487f3e1d83f04b4da279af25890edd960f551af21d875818593ed5`  
		Last Modified: Sat, 28 Apr 2018 13:04:11 GMT  
		Size: 114.1 MB (114061545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8a0f8df2121d204a18cd399908092bea4fde29f987d6f5bad24cfb0594fb41`  
		Last Modified: Sat, 28 Apr 2018 15:47:41 GMT  
		Size: 4.4 KB (4436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd02851236917aaa92099933e5faffebb116f1f40fb04d604096b1d127b303e`  
		Last Modified: Sat, 28 Apr 2018 15:47:41 GMT  
		Size: 117.7 KB (117650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4becd55e2977f430f40e123635843af05b784dce8a0283646c6f2fd5cb787ba`  
		Last Modified: Sat, 28 Apr 2018 15:47:48 GMT  
		Size: 17.7 MB (17712575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebb582b28d550ea5045143a4d7f03f89107c83c539a72731849ec698420abf7`  
		Last Modified: Sat, 28 Apr 2018 15:47:41 GMT  
		Size: 1.1 MB (1061049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7a9716647f9b33828d0101297165fa8dc830f99791592042c639447a4a4202`  
		Last Modified: Sat, 28 Apr 2018 15:48:27 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:9-onbuild` - linux; arm64 variant v8

```console
$ docker pull node@sha256:c9149023729cf180118532bba06c4d12039fa0475cad419f57adfce93b3badc1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245250511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d52cba86d38b920cc53d3b182effb876da4fefe08d076574cef51644ff4bbf3`
-	Default Command: `["npm","start"]`

```dockerfile
# Mon, 30 Apr 2018 23:21:38 GMT
ADD file:387c83918422a6546379c4d84818ca3949fcd63aec058da562b08c947a9ed571 in / 
# Mon, 30 Apr 2018 23:21:40 GMT
CMD ["bash"]
# Tue, 01 May 2018 07:39:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 May 2018 07:39:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 May 2018 07:42:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 May 2018 07:51:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 May 2018 12:50:50 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 01 May 2018 12:50:53 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 01 May 2018 12:50:54 GMT
ENV NODE_VERSION=9.11.1
# Tue, 01 May 2018 12:51:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Tue, 01 May 2018 12:51:04 GMT
ENV YARN_VERSION=1.5.1
# Tue, 01 May 2018 12:51:09 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Tue, 01 May 2018 12:51:10 GMT
CMD ["node"]
# Tue, 01 May 2018 12:51:24 GMT
RUN mkdir -p /usr/src/app
# Tue, 01 May 2018 12:51:25 GMT
WORKDIR /usr/src/app
# Tue, 01 May 2018 12:51:26 GMT
ONBUILD ARG NODE_ENV
# Tue, 01 May 2018 12:51:27 GMT
ONBUILD ENV NODE_ENV $NODE_ENV
# Tue, 01 May 2018 12:51:28 GMT
ONBUILD COPY package.json /usr/src/app/
# Tue, 01 May 2018 12:51:29 GMT
ONBUILD RUN npm install && npm cache clean --force
# Tue, 01 May 2018 12:51:30 GMT
ONBUILD COPY . /usr/src/app
# Tue, 01 May 2018 12:51:30 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:363cfded2ef3921ef972c85cafc77cf16cdcfddfd49782ad4540cb73fd5e57a2`  
		Last Modified: Mon, 30 Apr 2018 23:41:06 GMT  
		Size: 51.4 MB (51446854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ab1956443782680cb03e43882013be70cd0dded9f08b67f348f4c326e730b6`  
		Last Modified: Tue, 01 May 2018 08:52:49 GMT  
		Size: 17.2 MB (17192945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab7de614af5e80a6f3ed2459a7c31d96f56ce622eef6e74e9c56065255e8da9`  
		Last Modified: Tue, 01 May 2018 08:53:21 GMT  
		Size: 41.0 MB (41022228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c1966bf2c11ccb26c3e774d1a1638a729af08588bd7a91d7f8fab4dc192b85`  
		Last Modified: Tue, 01 May 2018 08:54:12 GMT  
		Size: 115.9 MB (115887927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c4117cadd6a899fcb6112198952c50afe67db53e53564fdda31d38ab69559f`  
		Last Modified: Tue, 01 May 2018 13:04:49 GMT  
		Size: 4.4 KB (4438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbbce473f736db6e576c5e8b8d7921a4bcb1d7e76142ef0b3331e38f6810a01`  
		Last Modified: Tue, 01 May 2018 13:04:48 GMT  
		Size: 117.6 KB (117621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385d1cc92a27c8b09d9c7451f11440e51885bbaa2cc4f09c702c48efbd54d7e2`  
		Last Modified: Tue, 01 May 2018 13:04:56 GMT  
		Size: 18.5 MB (18517337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062c55bc29551eac472cb1d56fc6aee45b0071a85704b44c54a74010ac3fa84f`  
		Last Modified: Tue, 01 May 2018 13:04:50 GMT  
		Size: 1.1 MB (1061029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b91ed62cc4db76502b2f85280e84caed2cfdd3280c04dc471951b0aca56d7a`  
		Last Modified: Tue, 01 May 2018 13:05:21 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:9-onbuild` - linux; 386

```console
$ docker pull node@sha256:d5b983ad899edcf3ad2e01f12da814d5e63cfed47f1ecebd074993fca5883af5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272717265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf008bcb03b2e6f7d2dc96aaaf1c2cf4285cc73e561c5d93895ef185df7e04e`
-	Default Command: `["npm","start"]`

```dockerfile
# Sat, 28 Apr 2018 10:39:32 GMT
ADD file:ce5174f2b2c155a2421fac3ff37a02d9551d5d79e31a541189bcfd2416a6903a in / 
# Sat, 28 Apr 2018 10:39:32 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 12:05:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 12:05:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 12:06:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 12:08:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 19:37:18 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 19:37:25 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 19:37:25 GMT
ENV NODE_VERSION=9.11.1
# Sat, 28 Apr 2018 19:37:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 19:37:32 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 19:37:35 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 19:37:35 GMT
CMD ["node"]
# Sat, 28 Apr 2018 19:37:40 GMT
RUN mkdir -p /usr/src/app
# Sat, 28 Apr 2018 19:37:40 GMT
WORKDIR /usr/src/app
# Sat, 28 Apr 2018 19:37:40 GMT
ONBUILD ARG NODE_ENV
# Sat, 28 Apr 2018 19:37:40 GMT
ONBUILD ENV NODE_ENV $NODE_ENV
# Sat, 28 Apr 2018 19:37:40 GMT
ONBUILD COPY package.json /usr/src/app/
# Sat, 28 Apr 2018 19:37:41 GMT
ONBUILD RUN npm install && npm cache clean --force
# Sat, 28 Apr 2018 19:37:41 GMT
ONBUILD COPY . /usr/src/app
# Sat, 28 Apr 2018 19:37:41 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:05b419d667f793c8c2edf0ff0aec14fc4d66733cdb89957ac89e8bfbeaddd0fa`  
		Last Modified: Sat, 28 Apr 2018 10:44:20 GMT  
		Size: 54.5 MB (54486782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b9c3b7ebe34e933c240e5eb7f8620732974e6e15e2c5d17cb91ca2aefffa4`  
		Last Modified: Sat, 28 Apr 2018 12:41:22 GMT  
		Size: 19.9 MB (19866118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95c26c8327697a43fa28c5661dbe845de5d6f433ed1e10ea672b26239f4b303`  
		Last Modified: Sat, 28 Apr 2018 12:41:52 GMT  
		Size: 43.9 MB (43918744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa73e6f1dcfd5115ba8ba791106f71c69c381615a3db75b9723e7a9e9a697a3`  
		Last Modified: Sat, 28 Apr 2018 12:42:40 GMT  
		Size: 135.1 MB (135146517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f6e1f764bad634e4257d786f5f9d3c8a11148f3c2b5dac448e955eca830ffc`  
		Last Modified: Sat, 28 Apr 2018 19:45:15 GMT  
		Size: 4.4 KB (4407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af6be7ca1b869f7780a379ab750e11ffb4719dc4170ca3a53e46571dd91200c`  
		Last Modified: Sat, 28 Apr 2018 19:45:15 GMT  
		Size: 117.6 KB (117625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c756c6ba584a2b1a9bcc96ba62d9b184434c5b86dff49a9e0e9fcac1122ec442`  
		Last Modified: Sat, 28 Apr 2018 19:45:20 GMT  
		Size: 18.1 MB (18115919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46de89b63cc9338a34f22e9a70e139ae9419a9fca652f366574397aba1dba46`  
		Last Modified: Sat, 28 Apr 2018 19:45:15 GMT  
		Size: 1.1 MB (1061021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb33c51da7b318d54f2606f83cf66827c4826348428357e498b24dedec07bbf`  
		Last Modified: Sat, 28 Apr 2018 19:45:41 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:9-onbuild` - linux; ppc64le

```console
$ docker pull node@sha256:67a8074b6b43d719e87fb0fbddb16025d65e14f486e5e583e40a0d39023b3aa9
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256209045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4cc94f009a3d15098de1b28ba0037fc340b676e3ff05b496497650be60a0bf`
-	Default Command: `["npm","start"]`

```dockerfile
# Sat, 28 Apr 2018 08:17:46 GMT
ADD file:6a4bd4ea54f669286e984ecf8178e1fa7c12c8b6fc0f96e4203ae7a6f99a2279 in / 
# Sat, 28 Apr 2018 08:17:47 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 09:53:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 09:53:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 09:55:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 09:58:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 15:45:36 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 15:45:43 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 15:45:44 GMT
ENV NODE_VERSION=9.11.1
# Sat, 28 Apr 2018 15:45:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 15:45:59 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 15:46:07 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 15:46:10 GMT
CMD ["node"]
# Sat, 28 Apr 2018 15:48:16 GMT
RUN mkdir -p /usr/src/app
# Sat, 28 Apr 2018 15:48:17 GMT
WORKDIR /usr/src/app
# Sat, 28 Apr 2018 15:48:18 GMT
ONBUILD ARG NODE_ENV
# Sat, 28 Apr 2018 15:48:19 GMT
ONBUILD ENV NODE_ENV $NODE_ENV
# Sat, 28 Apr 2018 15:48:20 GMT
ONBUILD COPY package.json /usr/src/app/
# Sat, 28 Apr 2018 15:48:22 GMT
ONBUILD RUN npm install && npm cache clean --force
# Sat, 28 Apr 2018 15:48:23 GMT
ONBUILD COPY . /usr/src/app
# Sat, 28 Apr 2018 15:48:24 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:2668401c9f940b1d6b03e5f0086fa248cb957610ef9a7c79983d2fb0707ec76c`  
		Last Modified: Sat, 28 Apr 2018 08:24:36 GMT  
		Size: 53.4 MB (53392811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73feb4c62e83f77f05ed3c1a72c453fce29bc8adee3ff31855937f28f0b9ad00`  
		Last Modified: Sat, 28 Apr 2018 10:38:43 GMT  
		Size: 17.6 MB (17571133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9e426fcbdcb0192ea4862cc89ecfe1a4ca0be8efaf99ffb329e50214efbd39`  
		Last Modified: Sat, 28 Apr 2018 10:39:15 GMT  
		Size: 42.8 MB (42758993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d8fbb2f05708fe70164cd6e8a92baac6ee3b432a7506f532fb94d5c94c19db`  
		Last Modified: Sat, 28 Apr 2018 10:40:09 GMT  
		Size: 123.0 MB (122994692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16adf06f7f47b565502a1950017a776278b81cccab32208d6f85e3c714bc9fc`  
		Last Modified: Sat, 28 Apr 2018 16:31:16 GMT  
		Size: 4.5 KB (4454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da032ac07e7c0a88767cd35630b8133da04e0ba79e7d77d5391bf8f923d5ca4`  
		Last Modified: Sat, 28 Apr 2018 16:31:15 GMT  
		Size: 117.7 KB (117652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79552354eab9797c1ee97003a56240b4aa24e945b10b7197cf30aed8e872a031`  
		Last Modified: Sat, 28 Apr 2018 16:31:34 GMT  
		Size: 18.3 MB (18308094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d4e5545c7a87e81f952e4c06031ea0e703b1968654fabedc8d45c163bcfc91`  
		Last Modified: Sat, 28 Apr 2018 16:31:15 GMT  
		Size: 1.1 MB (1061051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc0828a6ea34632617e7be63959788e9d6fb2e5124b958fd7ca850a605f45b4`  
		Last Modified: Sat, 28 Apr 2018 16:32:14 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:9-onbuild` - linux; s390x

```console
$ docker pull node@sha256:a59708c7fcb12493bd062ea3078fd736ba4475963ba04ffc8803a817591ffceb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.8 MB (251791157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef4f77e6b0a890e96e4d198c56d0f6f1423130b76df120d9183d7a18d731cb7`
-	Default Command: `["npm","start"]`

```dockerfile
# Sat, 28 Apr 2018 11:42:31 GMT
ADD file:ac1cfec75c7e1898f2c9b7d17653da3684fdda7d14440ce16f1939bb66105cdc in / 
# Sat, 28 Apr 2018 11:42:31 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 13:13:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 13:13:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 13:14:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 13:15:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 16:08:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 16:08:17 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 16:08:17 GMT
ENV NODE_VERSION=9.11.1
# Sat, 28 Apr 2018 16:08:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 16:08:21 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 16:08:23 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 16:08:24 GMT
CMD ["node"]
# Sat, 28 Apr 2018 17:01:22 GMT
RUN mkdir -p /usr/src/app
# Sat, 28 Apr 2018 17:01:23 GMT
WORKDIR /usr/src/app
# Sat, 28 Apr 2018 17:01:23 GMT
ONBUILD ARG NODE_ENV
# Sat, 28 Apr 2018 17:01:23 GMT
ONBUILD ENV NODE_ENV $NODE_ENV
# Sat, 28 Apr 2018 17:01:23 GMT
ONBUILD COPY package.json /usr/src/app/
# Sat, 28 Apr 2018 17:01:23 GMT
ONBUILD RUN npm install && npm cache clean --force
# Sat, 28 Apr 2018 17:01:23 GMT
ONBUILD COPY . /usr/src/app
# Sat, 28 Apr 2018 17:01:24 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:e0524893a6d25f3e36c190fea678ecf1845e7c0d2ba833b077a429d64b943e0a`  
		Last Modified: Sat, 28 Apr 2018 11:47:52 GMT  
		Size: 54.5 MB (54465857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2331cf8e884c1052e19f6b80b3efb54a7163ab49bf54c631bd861332c232029f`  
		Last Modified: Sat, 28 Apr 2018 13:29:06 GMT  
		Size: 17.8 MB (17767296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c860ff3f5f8fa212ce1ae15a427adb816d72db912daaa8697a136499f7b0cc9`  
		Last Modified: Sat, 28 Apr 2018 13:29:44 GMT  
		Size: 43.4 MB (43390531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7fdbc5bacccb4bce08796fc1aa69186d4c77318f1c3e315aef84ba7617442a`  
		Last Modified: Sat, 28 Apr 2018 13:30:16 GMT  
		Size: 116.2 MB (116192695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96fa84b36e49f51a8e1a40802c25734c11899e354a662bda8566f1a72939f9b`  
		Last Modified: Sat, 28 Apr 2018 17:52:30 GMT  
		Size: 4.4 KB (4428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b35972d9d77c4ea3f690288b106f9d5caf2a7d0fe12a9e8f5c1aa4bdf67e4ea`  
		Last Modified: Sat, 28 Apr 2018 17:52:31 GMT  
		Size: 117.6 KB (117623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28257b266778c692f39b0f2c05552dc9c3556d9775392d136af92df3cb1d14a9`  
		Last Modified: Sat, 28 Apr 2018 17:52:35 GMT  
		Size: 18.8 MB (18791572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996cf63f25e23f7737086d2961cebddea3c0501b8792ab96f47806ce4b411a2e`  
		Last Modified: Sat, 28 Apr 2018 17:52:31 GMT  
		Size: 1.1 MB (1061024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7177b65a6795546bd36b280c4fad25703b12a0b826868db52c88f7817e6e7e7`  
		Last Modified: Sat, 28 Apr 2018 17:53:04 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
