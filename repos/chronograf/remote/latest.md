## `chronograf:latest`

```console
$ docker pull chronograf@sha256:e7bcb11fbcf32b87cfb1ab84cd70a2c6074d6e91e7f19296df1d9978f2cf09a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:ad1f450c65a0031a54cb6c5085ae26343b5a5b32c511ba6473ab8e32eafc292f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48546254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d72ae84c3fa40ba24d499155a9d1ca06f3050dbc898b29b7c0df9119d3c5c05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 Apr 2018 07:09:59 GMT
ADD file:ec5be7eec56a749752ca284359ece04f5eb0b981eac08b8855454c6b16e3893c in / 
# Sat, 28 Apr 2018 07:09:59 GMT
CMD ["bash"]
# Mon, 30 Apr 2018 04:58:29 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 04 May 2018 03:52:24 GMT
ENV CHRONOGRAF_VERSION=1.4.4.2
# Fri, 04 May 2018 03:52:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 04 May 2018 03:52:41 GMT
COPY file:30de17380b1f353617f3efd8df8d07d842ebdd75d750781b20cc7588a54c918d in /usr/share/chronograf/LICENSE 
# Fri, 04 May 2018 03:52:44 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Fri, 04 May 2018 03:52:44 GMT
EXPOSE 8888/tcp
# Fri, 04 May 2018 03:52:46 GMT
VOLUME [/var/lib/chronograf]
# Fri, 04 May 2018 03:52:53 GMT
COPY file:5e829c8058b054261083c78e0bc7ad8730ab2331be79c5c3e1b6b84993b3224b in /entrypoint.sh 
# Fri, 04 May 2018 03:52:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 04 May 2018 03:52:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f2aa67a397c49232112953088506d02074a1fe577f65dc2052f158a3e5da52e8`  
		Last Modified: Sat, 28 Apr 2018 09:31:20 GMT  
		Size: 22.5 MB (22496029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7349ac161b0096ca747527cd84d6b0616b3221a251b4064e3c96d535b1698b2`  
		Last Modified: Mon, 30 Apr 2018 05:21:13 GMT  
		Size: 4.5 MB (4500376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26f5eda3f01ddd6935baba5e8eb60c436d66c1d814a9b5c7b4eeed012fe976c`  
		Last Modified: Fri, 04 May 2018 03:56:20 GMT  
		Size: 21.5 MB (21525448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4746e244fd6364702ca162c382bce996325e28424d79222623a0d18d2e3033`  
		Last Modified: Fri, 04 May 2018 03:56:15 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc0d1b690b49e50e70dbf39fc4d9074cc58acdab570599c7673f10bee3dc253`  
		Last Modified: Fri, 04 May 2018 03:56:15 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7287f573eeb51a4068215caebb6c5c2ed0eb9169e756f92680f55f3ce70423f3`  
		Last Modified: Fri, 04 May 2018 03:56:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:9ec39e798ca4108cb923575fbb2b4925a7c594faf57502834a1e9bfec2910f0f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43105388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef404d777c73970844de1836c5ed1a5141ecd8c02ae3dba2735572c9842b89b8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 28 Apr 2018 12:04:59 GMT
ADD file:f8bb9e9954bfe2f550e8a786c4be1dd5fca4a373b82b372b80c163e5640bd5a4 in / 
# Sat, 28 Apr 2018 12:05:00 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 12:35:42 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 28 Apr 2018 12:36:14 GMT
ENV CHRONOGRAF_VERSION=1.4.4.1
# Sat, 28 Apr 2018 12:36:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Sat, 28 Apr 2018 12:36:33 GMT
COPY file:30de17380b1f353617f3efd8df8d07d842ebdd75d750781b20cc7588a54c918d in /usr/share/chronograf/LICENSE 
# Sat, 28 Apr 2018 12:36:34 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Sat, 28 Apr 2018 12:36:34 GMT
EXPOSE 8888/tcp
# Sat, 28 Apr 2018 12:36:35 GMT
VOLUME [/var/lib/chronograf]
# Sat, 28 Apr 2018 12:36:36 GMT
COPY file:5e829c8058b054261083c78e0bc7ad8730ab2331be79c5c3e1b6b84993b3224b in /entrypoint.sh 
# Sat, 28 Apr 2018 12:36:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Apr 2018 12:36:37 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6c8a025e90b325dd5af06b0297cc1608120a47d4ab0e1cedb26c8cda811091d6`  
		Last Modified: Sat, 28 Apr 2018 12:16:08 GMT  
		Size: 19.3 MB (19286790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9dd0c89825e53b7cc7525e90a3213c9f6ddf632cdeeaf6522a84e1f3a1bc675`  
		Last Modified: Sat, 28 Apr 2018 12:36:56 GMT  
		Size: 3.9 MB (3873102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d53d8fb616197b9bdc5515fa8e1ade2acd252be3714d87bfc462496a1dad889`  
		Last Modified: Sat, 28 Apr 2018 12:37:43 GMT  
		Size: 19.9 MB (19921099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ed87c34ee768de792cd52567c647a1461987acf2376d24f7302a2ca5aaab0d`  
		Last Modified: Sat, 28 Apr 2018 12:37:36 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8544c7c8cca2a0ef7d6f865e0a6c47626e8b3532f0ead95071d9262d15b931f`  
		Last Modified: Sat, 28 Apr 2018 12:37:36 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f729b673c6860ff9a6fcb2c103baa7f2d803b1b064d5fb19ee8cb7a186fc1d8c`  
		Last Modified: Sat, 28 Apr 2018 12:37:37 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2bcdaf376faf5632b04d54321859fd9d8af0b86e3075f95ad48a36ad70c117cc
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44570170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64235773815c60ba3e046448c0573806be2d3c27890913b4c4535fbe9fbcd293`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 30 Apr 2018 23:33:18 GMT
ADD file:d423aa6d423df239af0602fe8134c14cb277778de23c8553d629d3b4b510f38b in / 
# Mon, 30 Apr 2018 23:33:20 GMT
CMD ["bash"]
# Tue, 01 May 2018 09:04:10 GMT
RUN set -ex &&     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 04 May 2018 08:39:49 GMT
ENV CHRONOGRAF_VERSION=1.4.4.2
# Fri, 04 May 2018 08:40:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 04 May 2018 08:40:36 GMT
COPY file:30de17380b1f353617f3efd8df8d07d842ebdd75d750781b20cc7588a54c918d in /usr/share/chronograf/LICENSE 
# Fri, 04 May 2018 08:40:37 GMT
COPY file:8cfc239e035af78ba9337d25f99200091e0d054985fe0c87e60b767d7759d99d in /usr/share/chronograf/agpl-3.0.md 
# Fri, 04 May 2018 08:40:38 GMT
EXPOSE 8888/tcp
# Fri, 04 May 2018 08:40:39 GMT
VOLUME [/var/lib/chronograf]
# Fri, 04 May 2018 08:40:40 GMT
COPY file:5e829c8058b054261083c78e0bc7ad8730ab2331be79c5c3e1b6b84993b3224b in /entrypoint.sh 
# Fri, 04 May 2018 08:40:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 04 May 2018 08:40:41 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:18d6337cc9064ce5276eac2eb6da6c5fe3f204bc7f1392f5ad1ba468817c609e`  
		Last Modified: Mon, 30 Apr 2018 23:54:34 GMT  
		Size: 20.3 MB (20347907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1ed840f6129db27f8a762fcdc2e6f407b2189ce2f3f863723380f1dfd7df6e`  
		Last Modified: Tue, 01 May 2018 09:06:44 GMT  
		Size: 4.1 MB (4075078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76353a4707c5c6462003c2545c1ee656b11bdf6f4521af02e8a181123ae0258c`  
		Last Modified: Fri, 04 May 2018 08:41:14 GMT  
		Size: 20.1 MB (20122786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792ef7dcd22a5c94d225aae752de928b0e9a4f73f04852d34390bb46e27ca4c5`  
		Last Modified: Fri, 04 May 2018 08:41:05 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216a45b4c1cb0025f2980fe759d9a4e8ac8a5fc2985796a4cc18e4121b37acc0`  
		Last Modified: Fri, 04 May 2018 08:41:05 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2e6754f531be23451c80fb2c8750aeecdfd8a4dd663af4ef1b9e0f6761f1f9`  
		Last Modified: Fri, 04 May 2018 08:41:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
