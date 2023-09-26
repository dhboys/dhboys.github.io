---
title: CentOS7 && docker
author: dhboys
date: 2023-09-26
categories: [Linux, Docker]
tags: [favicon]
---

<H1>Docker install</H1>
> from 'https://docs.docker.com/engine/install/centos/'

1. 저장소 설정

    - yum-utils유틸리티를 제공하는 패키지를 설치 ```yum-config-manager``` 하고 저장소를 설정합니다.

        ```sudo yum install -y yum-utils``` 

        ```sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo```

2. 도커 엔진 설치

    1. Docker 엔진, 컨테이너d 및 Docker Compose를 설치```yum-config-manager``` 하고 저장소를 설정합니다.

        ```sudo yum install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin``` 

    2. 도커 시작
        ```sudo systemctl start docker```

    3. 이미지 를 실행하여 Docker 엔진 설치가 성공했는지 확인
        ```sudo docker run hello-world```

<H1>Docker 사용자 권한</H1>

1. docker 서치 시 자동으로 그룹 생성

2. docker 그룹에 사용자 추가   
    ```sudo usermod -aG docker USERNAME```

3. 그룹 변경 활성화   
    ```newgrp docker```

4. docker 명령어 사용 여부 테스트   
    ```docker container ls```   
    ```docker ps```
