## `openjdk:7-jdk-jessie`

```console
$ docker pull openjdk@sha256:6d63fab00f42ee635ba80b519d2525263a0137bce0278da194f097981681b0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `openjdk:7-jdk-jessie` - linux; amd64

```console
$ docker pull openjdk@sha256:4c97c8ab82e638beaae0155de65eea1e553865abce74989547c4ee32dc4fdfc3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245093680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90cf6059f805ece232e9ea48de6309e6e322e744a7482214563a65e53436eb77`
-	Default Command: `["bash"]`

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
# Tue, 01 May 2018 13:05:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 May 2018 13:05:23 GMT
ENV LANG=C.UTF-8
# Tue, 01 May 2018 13:05:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 01 May 2018 13:05:25 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 01 May 2018 13:05:25 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 01 May 2018 13:05:25 GMT
ENV JAVA_VERSION=7u171
# Tue, 01 May 2018 13:05:26 GMT
ENV JAVA_DEBIAN_VERSION=7u171-2.6.13-1~deb8u1
# Tue, 01 May 2018 13:06:19 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
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
	-	`sha256:3f5dab7f622e25deef1ca36b1831ced4c27ab6291face28dde199e6bcc0bb1a5`  
		Last Modified: Tue, 01 May 2018 17:37:18 GMT  
		Size: 828.0 KB (827992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15486a3d881cdc0be818398c264b99a474729dd18246856f961be5e1f29344ff`  
		Last Modified: Tue, 01 May 2018 17:37:18 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086516aa0e5d10715e810a83875512482326da778bed7c04f958cf38cf6a9028`  
		Last Modified: Tue, 01 May 2018 17:37:18 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e29b7b213a6cdfecccff97042be9eb5a55e087816c3f1010d761aa7c7821f23`  
		Last Modified: Tue, 01 May 2018 17:37:38 GMT  
		Size: 129.2 MB (129184541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:7-jdk-jessie` - linux; arm variant v5

```console
$ docker pull openjdk@sha256:96ff04409733ece84b084b3b075ae386268b495e5a51f0a1b9db941afe9eed9e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.0 MB (216018510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a131057f3ff2032c9e913593b731bf2c47ca72a64144656ea426937c261e302`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Apr 2018 08:49:23 GMT
ADD file:2d2cd360e66aeff5557c7e7117985a00d109278c3f456ee970afcc9a46483264 in / 
# Sat, 28 Apr 2018 08:49:23 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 09:24:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 09:24:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 09:25:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 12:56:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 12:56:53 GMT
ENV LANG=C.UTF-8
# Sat, 28 Apr 2018 12:56:55 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 28 Apr 2018 12:56:56 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 28 Apr 2018 12:56:56 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 28 Apr 2018 12:56:56 GMT
ENV JAVA_VERSION=7u171
# Sat, 28 Apr 2018 12:56:57 GMT
ENV JAVA_DEBIAN_VERSION=7u171-2.6.13-1~deb8u1
# Sat, 28 Apr 2018 12:58:02 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
```

-	Layers:
	-	`sha256:81fc0826192f72abe617753d378af4047dbce89faf17cdab9166877006a25d8e`  
		Last Modified: Sat, 28 Apr 2018 08:57:10 GMT  
		Size: 52.5 MB (52456037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229392eca0ea6fd4f2cc8f7d0d7ae06b4ee3b653f27de84082dfa6c08f937eb3`  
		Last Modified: Sat, 28 Apr 2018 09:38:39 GMT  
		Size: 17.1 MB (17054111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c50069643e7ba8c967fb7fe1d1d9a2f42e28ededf3d5c2744f7751f7371905e`  
		Last Modified: Sat, 28 Apr 2018 09:39:06 GMT  
		Size: 41.1 MB (41103326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04baab6490d64207af45c8888b3cb629c8e206e86fe46e7c086e66b72f15e3ab`  
		Last Modified: Sat, 28 Apr 2018 13:30:59 GMT  
		Size: 821.2 KB (821210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b63c4c8cfd5a88398e29e1c37872dbc5ec79c7ce76fd9e655c53d580cb8c03`  
		Last Modified: Sat, 28 Apr 2018 13:30:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab14fc3b5d61eb452bf584bf6e7eac54e2ed4fe68d732283c610dc4ebb9b075a`  
		Last Modified: Sat, 28 Apr 2018 13:30:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a35b148fd246635cb33f8c7859d52171d6123a7a8e8f64690059ea8431b700b`  
		Last Modified: Sat, 28 Apr 2018 13:31:22 GMT  
		Size: 104.6 MB (104583448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:7-jdk-jessie` - linux; arm variant v7

```console
$ docker pull openjdk@sha256:e5bc05e31c76819f563532d19df94697db5f2577948605972d996729021784e2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220491510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1923170b64899bce2aa1b3df6890fb63f46c58b9d636845d6a78f546ce125a76`
-	Default Command: `["bash"]`

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
# Sat, 28 Apr 2018 12:59:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 12:59:58 GMT
ENV LANG=C.UTF-8
# Sat, 28 Apr 2018 13:00:00 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 28 Apr 2018 13:00:01 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 28 Apr 2018 13:00:01 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 28 Apr 2018 13:00:02 GMT
ENV JAVA_VERSION=7u171
# Sat, 28 Apr 2018 13:00:02 GMT
ENV JAVA_DEBIAN_VERSION=7u171-2.6.13-1~deb8u1
# Sat, 28 Apr 2018 13:01:20 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
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
	-	`sha256:aef0272ce28906e34cb64ac14f4639b57aaed33d4ad65d30e3668719dc712afe`  
		Last Modified: Sat, 28 Apr 2018 13:28:59 GMT  
		Size: 795.1 KB (795139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd14ec28b169d4d3d4305399c1d6ee52a8aa1964daa47a6643dd855e2cdf6a4`  
		Last Modified: Sat, 28 Apr 2018 13:28:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7053dbe1e4b66db8ee573619e06992fdb94142f2939d21dca74e654b33db3b`  
		Last Modified: Sat, 28 Apr 2018 13:28:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635db2b83017cddee41c0f87e68880a00336d0b4543262ca38d5b193df4e9bc8`  
		Last Modified: Sat, 28 Apr 2018 13:29:20 GMT  
		Size: 113.0 MB (113034409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:7-jdk-jessie` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:967df905e5b8c9b432e08149c8cfb930f18c252b200cec4d5619b66703a15b95
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215013728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e942e07cae5d6a728cdbc1dd5ad0a67a3fd3c94276a27eb23d2641063e12d4e`
-	Default Command: `["bash"]`

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
# Tue, 01 May 2018 11:27:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 May 2018 11:27:16 GMT
ENV LANG=C.UTF-8
# Tue, 01 May 2018 11:27:19 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 01 May 2018 11:27:22 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 01 May 2018 11:27:27 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 01 May 2018 11:27:28 GMT
ENV JAVA_VERSION=7u171
# Tue, 01 May 2018 11:27:33 GMT
ENV JAVA_DEBIAN_VERSION=7u171-2.6.13-1~deb8u1
# Tue, 01 May 2018 11:34:47 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
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
	-	`sha256:5ccdb3c56ce18c3bdfa45e737689bbf55c06eefcff8df02bd36fc2e9d4e73033`  
		Last Modified: Tue, 01 May 2018 11:59:48 GMT  
		Size: 823.2 KB (823229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc074bffb3a41a1364f30d9742cc6b0ef76de147c256f3316e927ab183171fce`  
		Last Modified: Tue, 01 May 2018 11:59:48 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18536f0b7e342720012eeedb406f76c2a7126766ba860444beae200086cd2bee`  
		Last Modified: Tue, 01 May 2018 11:59:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc39dcaa0afbcb917b6c48d857fce184e79e5efc4a1ce0a3ff32c7d30b0e79a`  
		Last Modified: Tue, 01 May 2018 12:00:11 GMT  
		Size: 104.5 MB (104528094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:7-jdk-jessie` - linux; 386

```console
$ docker pull openjdk@sha256:55d8d85e35c9f769f547b99c4be7328d50e291b1e161fcd15a188336be9221e7
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 MB (259423796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a6d6db7b593db09a3ab8856271d1613cae5844d0456925df996f59da60f050`
-	Default Command: `["bash"]`

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
# Sat, 28 Apr 2018 15:01:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 15:01:11 GMT
ENV LANG=C.UTF-8
# Sat, 28 Apr 2018 15:01:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 28 Apr 2018 15:01:12 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 28 Apr 2018 15:01:12 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 28 Apr 2018 15:01:12 GMT
ENV JAVA_VERSION=7u171
# Sat, 28 Apr 2018 15:01:13 GMT
ENV JAVA_DEBIAN_VERSION=7u171-2.6.13-1~deb8u1
# Sat, 28 Apr 2018 15:02:21 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
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
	-	`sha256:8a2328ba7d674177da9705f75d81ca4bff867ef6db908ba6f60d10b58cc309f4`  
		Last Modified: Sat, 28 Apr 2018 15:26:26 GMT  
		Size: 830.9 KB (830878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2404371b1c7c44cae166412120eb3f88a0fbe6d4ec372be8763d7952d0457840`  
		Last Modified: Sat, 28 Apr 2018 15:26:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c602a26e36dc7833114449ade05dc3a770229f492fd4b678252d76d3a06f6e`  
		Last Modified: Sat, 28 Apr 2018 15:26:26 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8517a671b32476cc1e408cc2f3b917d24b1d04c8a955226d09a0afb4bb0294`  
		Last Modified: Sat, 28 Apr 2018 15:26:55 GMT  
		Size: 140.3 MB (140320896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:7-jdk-jessie` - linux; ppc64le

```console
$ docker pull openjdk@sha256:a00a2a90a1c25fc37ee9c03f8d27a8a1d8d7e2bcd925dec4036850624592406b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220729866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3534a9beb25662d01e622322198d70612aa9db42bd593ad257454625791c143`
-	Default Command: `["bash"]`

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
# Sat, 28 Apr 2018 17:48:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 17:48:42 GMT
ENV LANG=C.UTF-8
# Sat, 28 Apr 2018 17:48:44 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 28 Apr 2018 17:48:47 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 28 Apr 2018 17:48:48 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 28 Apr 2018 17:48:48 GMT
ENV JAVA_VERSION=7u171
# Sat, 28 Apr 2018 17:48:49 GMT
ENV JAVA_DEBIAN_VERSION=7u171-2.6.13-1~deb8u1
# Sat, 28 Apr 2018 17:53:03 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
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
	-	`sha256:bbddf27467c15887bbdf6a7c8ab56e10dec2948c970ca41320b7f831fae5364c`  
		Last Modified: Sat, 28 Apr 2018 18:10:43 GMT  
		Size: 823.5 KB (823457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178316777b97bdf560e8150d0c757e59aaedab16beb6f78767f28dca6d4aa1af`  
		Last Modified: Sat, 28 Apr 2018 18:10:43 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca176f5012b850a526ea46ab2f6ffe331129c0ea8694c670d3eab1e088945f48`  
		Last Modified: Sat, 28 Apr 2018 18:10:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ba2ea2d9ffb7fb26e09e0be4f5e3beb6a86d79ad5f6525d7265e83e0e6d613`  
		Last Modified: Sat, 28 Apr 2018 18:11:01 GMT  
		Size: 106.2 MB (106183093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:7-jdk-jessie` - linux; s390x

```console
$ docker pull openjdk@sha256:b927346557edb177030cc44458d4af52939d6094b95c8b9b5ad8c984a93f5338
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.6 MB (221628636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b71e84c0b97e89aff0f09d0baf3df0ee11add3198c4f3bd6496d34c7a133c31`
-	Default Command: `["bash"]`

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
# Sat, 28 Apr 2018 14:34:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 14:34:23 GMT
ENV LANG=C.UTF-8
# Sat, 28 Apr 2018 14:34:24 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 28 Apr 2018 14:34:24 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 28 Apr 2018 14:34:25 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 28 Apr 2018 14:34:25 GMT
ENV JAVA_VERSION=7u171
# Sat, 28 Apr 2018 14:34:25 GMT
ENV JAVA_DEBIAN_VERSION=7u171-2.6.13-1~deb8u1
# Sat, 28 Apr 2018 14:35:02 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
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
	-	`sha256:f89b0770fb1b649b8857f5f768ba3021ff4468fa78ca5286a83dc069a3c4433b`  
		Last Modified: Sat, 28 Apr 2018 14:59:14 GMT  
		Size: 837.3 KB (837261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0241c93015056e7e5ae4437e8932852dedd1252a7fce2c3ae1db34ce7a64e71`  
		Last Modified: Sat, 28 Apr 2018 14:59:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434b96db40a71a9a25ced0ba0af5f3a992dcb5fb2d1569bc5623b17b5d9a885c`  
		Last Modified: Sat, 28 Apr 2018 14:59:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8407cfb82f0263e8b7ab2ab3b6fa9c71d7fe5fafcd6fd068a4789dfd9852f6`  
		Last Modified: Sat, 28 Apr 2018 14:59:25 GMT  
		Size: 105.2 MB (105167313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
