## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:d120628ab5b043c4134e8089033fb1be2b19ea867988fc8242afa5a50dac3ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:4960b132f7f5e373447ef7e6a92167ba43f3ed27bbeb3e58e65d98014d569306
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96010338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d007b18fcc8364571f0efb45a1413c75beb43c054946863782ffae2cdd12f753`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 28 Apr 2018 07:08:53 GMT
ADD file:9572fdb59dfbb9b032f3331bbc2a08b31e0aef5fbde44c8f2008d22bf5290cf2 in / 
# Sat, 28 Apr 2018 07:08:53 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 17:03:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 17:03:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 May 2018 21:01:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 02 May 2018 21:01:57 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 02 May 2018 21:02:28 GMT
ENV KAPACITOR_VERSION=1.4.1
# Wed, 02 May 2018 21:02:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Wed, 02 May 2018 21:02:53 GMT
COPY file:4046787774ea4c49703132e9dbc6fb3a19cb54632aa7032dd8379f12b56034d9 in /etc/kapacitor/kapacitor.conf 
# Wed, 02 May 2018 21:02:53 GMT
EXPOSE 9092/tcp
# Wed, 02 May 2018 21:02:53 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 02 May 2018 21:02:54 GMT
COPY file:e5d90b0779cb7845ca3a7981c04a97fd959fea211a2ce19c8da8b949f9d9d04c in /entrypoint.sh 
# Wed, 02 May 2018 21:02:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 May 2018 21:02:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:cc1a78bfd46becbfc3abb8a74d9a70a0e0dc7a5809bbd12e814f9382db003707`  
		Last Modified: Sat, 28 Apr 2018 09:27:54 GMT  
		Size: 45.3 MB (45318159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c14872d9970c08665f5dd1b41a6adfb11583b8337c0f9236dcd23e093a4f02`  
		Last Modified: Sat, 28 Apr 2018 20:46:10 GMT  
		Size: 10.7 MB (10747762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ae159b9cae5ecb1a10a4acd04b700b23bfb8293d616bc9efd9aa234b0c1fc3`  
		Last Modified: Sat, 28 Apr 2018 20:46:09 GMT  
		Size: 4.3 MB (4335353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6242bdbc6ef2bb9219c5128a49cc8f207828e799593b58ff6ae44a9e2a20a7`  
		Last Modified: Wed, 02 May 2018 21:03:25 GMT  
		Size: 12.9 MB (12912044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21a07fb939435fbb698acaf8f14a9f2afee6afd7b34ccc38343940cac995070`  
		Last Modified: Wed, 02 May 2018 21:03:24 GMT  
		Size: 2.9 KB (2890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd28f636c12efc1fad8c423ac6e151a0bade6fe9f6e1f39ccef5e71798152095`  
		Last Modified: Wed, 02 May 2018 21:04:21 GMT  
		Size: 22.7 MB (22693675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6878e2a8641e65378324af58e9981e306316837b70c01d89a4500a5fb4676e`  
		Last Modified: Wed, 02 May 2018 21:04:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b2f15f511fc6f465f04eb4cbda4a5c81566a89fb22e0695bab65ba081dc4df`  
		Last Modified: Wed, 02 May 2018 21:04:18 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:02570317f38282fd3c0f72bd645083bd2ba20a9d3614f006f8c304568448321b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89823599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77c5b84655752fafa9203850705ed4f9830c4594de50df6108a5a4130a9481a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 28 Apr 2018 12:04:18 GMT
ADD file:c7fba27b02c4bda63faef7eb30156a55feb4c0e9ecd529a24dd8d62942c2f83c in / 
# Sat, 28 Apr 2018 12:04:19 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 12:42:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 12:42:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 15:58:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 28 Apr 2018 15:58:15 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Sat, 28 Apr 2018 15:58:34 GMT
ENV KAPACITOR_VERSION=1.4.1
# Sat, 28 Apr 2018 15:58:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Sat, 28 Apr 2018 15:58:41 GMT
COPY file:4046787774ea4c49703132e9dbc6fb3a19cb54632aa7032dd8379f12b56034d9 in /etc/kapacitor/kapacitor.conf 
# Sat, 28 Apr 2018 15:58:41 GMT
EXPOSE 9092/tcp
# Sat, 28 Apr 2018 15:58:42 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 28 Apr 2018 15:58:42 GMT
COPY file:e5d90b0779cb7845ca3a7981c04a97fd959fea211a2ce19c8da8b949f9d9d04c in /entrypoint.sh 
# Sat, 28 Apr 2018 15:58:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Apr 2018 15:58:43 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:5483105d09166836731e940c850827dd1a4fe16b04d1921eea4d8da7c98e99bc`  
		Last Modified: Sat, 28 Apr 2018 12:15:18 GMT  
		Size: 42.1 MB (42063737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb5424e9076ab96c3fbc714afcd99e7f9c4f35ecf54660ae99cf71410315613`  
		Last Modified: Sat, 28 Apr 2018 13:06:40 GMT  
		Size: 9.4 MB (9449717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed44b64a3aee0cea1bad2a1954b943ef678d795d9c3ac814e5f8bbbc99a9b143`  
		Last Modified: Sat, 28 Apr 2018 13:06:38 GMT  
		Size: 3.9 MB (3912466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34b2ddb3b552ef7886565e790e578fdea57fd1f1650062913037b31514acb7a`  
		Last Modified: Sat, 28 Apr 2018 15:59:00 GMT  
		Size: 13.1 MB (13086847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910958468cf599d5695794edeab6afb693ebbdfbf8b4067c6b778b6fa189d2aa`  
		Last Modified: Sat, 28 Apr 2018 15:59:01 GMT  
		Size: 2.9 KB (2916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed9540470ca94ee026756badfc0f32ca1412b3f34a7f660c9a4dae8df3dee28`  
		Last Modified: Sat, 28 Apr 2018 15:59:32 GMT  
		Size: 21.3 MB (21307461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dc7af5fdf97b6be94c6384c49bf02c91995655a00944417384bacee697b493`  
		Last Modified: Sat, 28 Apr 2018 15:59:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed9b0db2d2a6ebfa93c9b77e02c8705c85927dc1c595c4f0f1893738ebb76c0`  
		Last Modified: Sat, 28 Apr 2018 15:59:24 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:dead948648d8510a034b17e18868e24fb0f658f2eb3737f4ac9adbd58a30821d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90825207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc982147ebe5ddacbfb9e6b62a95af7ed73c309ffd961f5de5b712fbe6a34e4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 30 Apr 2018 23:31:58 GMT
ADD file:245a8cfe59ea071e4e215a722e0d4b4b14fa95dd6ffd03739fe048433cfaf523 in / 
# Mon, 30 Apr 2018 23:32:00 GMT
CMD ["bash"]
# Tue, 01 May 2018 08:07:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 May 2018 08:08:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 May 2018 15:04:43 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 01 May 2018 15:04:48 GMT
RUN set -ex &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Tue, 01 May 2018 15:05:28 GMT
ENV KAPACITOR_VERSION=1.4.1
# Tue, 01 May 2018 15:05:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Tue, 01 May 2018 15:05:43 GMT
COPY file:4046787774ea4c49703132e9dbc6fb3a19cb54632aa7032dd8379f12b56034d9 in /etc/kapacitor/kapacitor.conf 
# Tue, 01 May 2018 15:05:44 GMT
EXPOSE 9092/tcp
# Tue, 01 May 2018 15:05:45 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 01 May 2018 15:05:46 GMT
COPY file:e5d90b0779cb7845ca3a7981c04a97fd959fea211a2ce19c8da8b949f9d9d04c in /entrypoint.sh 
# Tue, 01 May 2018 15:05:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 May 2018 15:05:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:142bf25d8d1b3ebc9dfbedd586e70a011594690acf48b2695bfce01e3a2cf0d5`  
		Last Modified: Mon, 30 Apr 2018 23:52:13 GMT  
		Size: 43.1 MB (43109349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe3c77baf3b64937d2b7b343d9b966a08f6b90568acce53ff6effca0fd787fe`  
		Last Modified: Tue, 01 May 2018 08:57:09 GMT  
		Size: 9.7 MB (9697043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769a11625fb0ec33902994bfc5463ff53a6754be4cd51b8dc5ca168a05228b09`  
		Last Modified: Tue, 01 May 2018 08:57:06 GMT  
		Size: 4.1 MB (4087722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8180e4b44a1dbd262ed2dc74857b028173cdae911302228e2d18f0a1723d9124`  
		Last Modified: Tue, 01 May 2018 15:06:19 GMT  
		Size: 12.6 MB (12620487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ea43aa800755810b5d65e42efbe96df973b1bed67e44f7811a274600690407`  
		Last Modified: Tue, 01 May 2018 15:06:12 GMT  
		Size: 2.9 KB (2884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730282be6e71cdfdc60b5ffbaed52f89e14a683dc70a82c383ab16323f057839`  
		Last Modified: Tue, 01 May 2018 15:06:53 GMT  
		Size: 21.3 MB (21307267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e22aff35515d9b03b795595ef1f4b278d093d4094fe048c6dd3c0fe1af00c4`  
		Last Modified: Tue, 01 May 2018 15:06:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe0084fb06cb3f6839b709e6e73e77469989dbcc55872f871517b41103afe39`  
		Last Modified: Tue, 01 May 2018 15:06:44 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
