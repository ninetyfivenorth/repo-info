## `groovy:jre7`

```console
$ docker pull groovy@sha256:f573286fdb2d68d96988508d6f21efadab76386d1fc7a2abc2a385c07f59203f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `groovy:jre7` - linux; amd64

```console
$ docker pull groovy@sha256:9a826e4302bca873ddeebe70833769d716491522c3b9cdccc983c78194a9a4fd
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227308345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22dcdddf7d0fc58b6a3754af6dae5561c965238ccb4e681dc35629c4c2fd23c`
-	Default Command: `["groovysh"]`

```dockerfile
# Tue, 13 Mar 2018 21:57:21 GMT
ADD file:bc844c4763367b5f0ac7b9aebf7d43900d98f2aca101b886f185347b24973dbe in / 
# Tue, 13 Mar 2018 21:57:22 GMT
CMD ["bash"]
# Tue, 13 Mar 2018 23:39:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Mar 2018 23:39:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 14 Mar 2018 11:12:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 11:12:58 GMT
ENV LANG=C.UTF-8
# Wed, 14 Mar 2018 11:12:59 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 14 Mar 2018 11:12:59 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 14 Mar 2018 11:13:00 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 10 Apr 2018 03:38:22 GMT
ENV JAVA_VERSION=7u171
# Tue, 10 Apr 2018 03:38:22 GMT
ENV JAVA_DEBIAN_VERSION=7u171-2.6.13-1~deb8u1
# Tue, 10 Apr 2018 03:39:31 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jre="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 10 Apr 2018 06:36:16 GMT
CMD ["groovysh"]
# Tue, 10 Apr 2018 06:36:16 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 10 Apr 2018 06:36:16 GMT
ENV GROOVY_VERSION=2.4.15
# Tue, 10 Apr 2018 06:36:44 GMT
RUN set -o errexit -o nounset 	&& echo "Downloading Groovy" 	&& wget --no-verbose --output-document=groovy.zip "https://dist.apache.org/repos/dist/release/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip" 		&& echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server" 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in 		"7FAA0F2206DE228F0DB01AD741321490758AAD6F" 		"331224E1D7BE883D16E8A685825C06C827AF6B66" 		"34441E504A937F43EB0DAEF96A65176A0FB1CD0B" 		"9A810E3B766E089FFB27C70F11B595CEDC4AEBB5" 		"81CABC23EECA0790E8989B361FF96E10F0E13706" 	; do 		for server in 			"ha.pool.sks-keyservers.net" 			"hkp://p80.pool.sks-keyservers.net:80" 			"pgp.mit.edu" 		; do 			echo "  Trying ${server}"; 			if gpg --keyserver "${server}" --recv-keys "${key}"; then 				break; 			fi; 		done; 	done; 	if [ $(gpg --list-keys | grep -c "pub ") -ne 5 ]; then 		echo "ERROR: Failed to fetch GPG keys" >&2; 		exit 1; 	fi 		&& echo "Checking download signature" 	&& wget --no-verbose --output-document=groovy.zip.asc "https://dist.apache.org/repos/dist/release/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc" 	&& gpg --batch --verify groovy.zip.asc groovy.zip 	&& rm --recursive --force "${GNUPGHOME}" 	&& rm groovy.zip.asc 		&& echo "Installing Groovy" 	&& unzip groovy.zip 	&& rm groovy.zip 	&& mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/" 	&& ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape 	&& ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy 	&& ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc 	&& ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole 	&& ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc 	&& ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh 	&& ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy 		&& echo "Adding groovy user and group" 	&& groupadd --system --gid 1000 groovy 	&& useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy 	&& mkdir --parents /home/groovy/.groovy/grapes 	&& chown --recursive groovy:groovy /home/groovy 		&& echo "Symlinking root .groovy to groovy .groovy" 	&& ln -s /home/groovy/.groovy /root/.groovy
# Tue, 10 Apr 2018 06:36:44 GMT
USER [groovy]
# Tue, 10 Apr 2018 06:36:44 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 10 Apr 2018 06:36:44 GMT
WORKDIR /home/groovy
# Tue, 10 Apr 2018 06:36:48 GMT
RUN set -o errexit -o nounset 	&& echo "Testing Groovy installation" 	&& groovy --version
```

-	Layers:
	-	`sha256:f2b6b4884fc8b2f1fcef843f92f7c82c9c149df85ac77e5f0de7a342ae442412`  
		Last Modified: Tue, 13 Mar 2018 22:43:41 GMT  
		Size: 52.6 MB (52608519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb899b4df216ab398fb05547f86dc371db944cf53dea7913d2f4261ed09e2be`  
		Last Modified: Wed, 14 Mar 2018 00:34:40 GMT  
		Size: 19.3 MB (19266189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9837675e69408ed38a5cd50b7bad4aceb89b943ec4d0c6547d3da7c2911ce1fa`  
		Last Modified: Wed, 14 Mar 2018 13:15:40 GMT  
		Size: 795.6 KB (795622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d602d78cf3359ca712061598d8ff56eb3242af4ca83b5d1c650e8d2e37e70fe7`  
		Last Modified: Wed, 14 Mar 2018 13:15:39 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0d228baacbc3d4fd9bb4ed7dda30fee6eb4cee8a615c3c1f03215c6e2c8478`  
		Last Modified: Wed, 14 Mar 2018 13:15:39 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ed19f6416aabe363128cc92d55cf9ab0dc552903edf97bcbce2c98a824bac`  
		Last Modified: Tue, 10 Apr 2018 04:06:54 GMT  
		Size: 117.5 MB (117493710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2196b6e2f066e302ca54340969a4640af11cdd4c7252c754bca963a4ca36ea83`  
		Last Modified: Tue, 10 Apr 2018 07:05:41 GMT  
		Size: 37.1 MB (37143786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db9e193c7f1a3526f8c745bff7f0aa9eb44c6efb492463486edcff718133457`  
		Last Modified: Tue, 10 Apr 2018 07:05:37 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
