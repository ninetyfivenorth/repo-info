## `python:windowsservercore`

```console
$ docker pull python@sha256:eb554702c5102bc2bdb914bfdfe97c8265d080351902d2508853eab0f4bb2141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.2189; amd64
	-	windows version 10.0.16299.371; amd64

### `python:windowsservercore` - windows version 10.0.14393.2189; amd64

```console
$ docker pull python@sha256:5f1334d3fbdf60b5470839fcc3fd7972948bad1213bd80e56f6a9f3e2a4c2d33
```

-	Docker Version: 17.10.0-ee-preview-3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 GB (5456525963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4eacf3a5ef0dd74eb209f10bb4d7942a68cfb5211ac1de850230e3e803595b`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Fri, 06 Apr 2018 21:38:52 GMT
RUN Install update 10.0.14393.2189
# Fri, 27 Apr 2018 09:14:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 27 Apr 2018 09:36:33 GMT
ENV PYTHON_VERSION=3.6.5
# Fri, 27 Apr 2018 09:36:34 GMT
ENV PYTHON_RELEASE=3.6.5
# Fri, 27 Apr 2018 09:39:14 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.';
# Fri, 27 Apr 2018 09:39:15 GMT
ENV PYTHON_PIP_VERSION=10.0.1
# Fri, 27 Apr 2018 09:40:46 GMT
RUN Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri 'https://bootstrap.pypa.io/get-pip.py' -OutFile 'get-pip.py'; 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.';
# Fri, 27 Apr 2018 09:40:47 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 13 Dec 2016 10:53:31 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f3369c32b2e3183340664c2bd4babb9c71cedc116fba70fda326df3ef9e48cc`  
		Last Modified: Fri, 06 Apr 2018 21:38:52 GMT  
		Size: 1.3 GB (1324227515 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a34e69c38a84789216f85ca14f1cd2fd80f3bf47f351a2a3130f2b3241a8db39`  
		Last Modified: Fri, 27 Apr 2018 09:24:43 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780c39f7fac5b1c2da6d216caa00c34fe25841cb79d4050141ebb7a4e0295790`  
		Last Modified: Fri, 27 Apr 2018 09:55:52 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4c87ceab0300064b167b4cb40349655242a26d5b50fdfc55c22f79da675234`  
		Last Modified: Fri, 27 Apr 2018 09:55:47 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d055724a5f2cc1c5103eae78395da040ebe9be68e9e7d06f9aebcdc376b90f12`  
		Last Modified: Fri, 27 Apr 2018 09:56:13 GMT  
		Size: 52.5 MB (52488522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73251765a421429add0401329eb2599d1cafa6c9339a6a1483ece4b2d95c4c8`  
		Last Modified: Fri, 27 Apr 2018 09:55:47 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafc1aaa9881a7337b2ce24cd6d5a1ea948af5b182d071f33069a4a987f823e5`  
		Last Modified: Fri, 27 Apr 2018 09:56:01 GMT  
		Size: 9.8 MB (9818094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d16672abf3eaaceb993cb2ee488941ea8d3850377f20046687a1f00156fcbf`  
		Last Modified: Fri, 27 Apr 2018 09:55:47 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:windowsservercore` - windows version 10.0.16299.371; amd64

```console
$ docker pull python@sha256:0d57e55a6b2d390a4ee709d687238d1605c040dc54cbbc742ad53c67fcf0a21a
```

-	Docker Version: 17.10.0-ee-preview-3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3093100416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e061337edb31a9aafee0bbb18e68ca1f915a98891c36e4dced6a12459112dc8`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 29 Sep 2017 14:43:28 GMT
RUN Apply image 10.0.16299.15
# Mon, 02 Apr 2018 18:15:35 GMT
RUN Install update 10.0.16299.371
# Wed, 11 Apr 2018 09:40:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 27 Apr 2018 09:41:00 GMT
ENV PYTHON_VERSION=3.6.5
# Fri, 27 Apr 2018 09:41:00 GMT
ENV PYTHON_RELEASE=3.6.5
# Fri, 27 Apr 2018 09:43:12 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.';
# Fri, 27 Apr 2018 09:43:13 GMT
ENV PYTHON_PIP_VERSION=10.0.1
# Fri, 27 Apr 2018 09:44:30 GMT
RUN Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri 'https://bootstrap.pypa.io/get-pip.py' -OutFile 'get-pip.py'; 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.';
# Fri, 27 Apr 2018 09:44:31 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:5847a47b8593f7c39aa5e3db09e50b76d42aa8898c0440c70cc9c69747d4c479`  
		Last Modified: Tue, 17 Oct 2017 15:51:05 GMT  
		Size: 2.3 GB (2274300585 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2dd7b93d509d5e7086ff08713d58180cc639adf9536c560a2dca5bf7139f5323`  
		Last Modified: Tue, 10 Apr 2018 16:34:04 GMT  
		Size: 761.5 MB (761549625 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c87bca28288a632bcbf4a2a60ebf89a3e996de2cd79edec70cde506458b9b16c`  
		Last Modified: Thu, 26 Apr 2018 17:18:06 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32578d7d5005fd0d5169452505138fe6fdaafd1927d9ba656fe947a498ab8fa7`  
		Last Modified: Fri, 27 Apr 2018 09:56:34 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f9f0463b943e6d3a5538d4701311a7611cdb3c0182e3df73bf48e4263336ab`  
		Last Modified: Fri, 27 Apr 2018 09:56:31 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f2cdf2b3a07c143c381ba5e710e54a7a36fb2b30067be68d7e764190b6f22c`  
		Last Modified: Fri, 27 Apr 2018 09:56:57 GMT  
		Size: 47.8 MB (47754395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66006643fb4b829a11db5269ee442f09790aa25723d749a09714593302b15d4`  
		Last Modified: Fri, 27 Apr 2018 09:56:30 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815aeb2a0db02768e3cd90ff32ca1cb4b5e1fb237925e57cd0dff5f9be651454`  
		Last Modified: Fri, 27 Apr 2018 09:56:43 GMT  
		Size: 9.5 MB (9489821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96322fea3eae1faf0558132701c3d7ad90636c0c652a08a031cfa4839f65f40d`  
		Last Modified: Fri, 27 Apr 2018 09:56:31 GMT  
		Size: 1.2 KB (1197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
