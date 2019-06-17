# opensource COBOL for Docker

opensource COBOL and Open COBOL ESQL development environment

Versions :
- CentOS: centos7
- opensource COBOL: 1.5.2J
- Open COBOL ESQL: 1.2

Sample :

sample cobol run on docker image.

```
mkdir src
wget -O src/HELLO.cbl https://raw.githubusercontent.com/opensourcecobol/oc-dockerfile/master/HELLO.cbl
docker pull opensourcecobol/opensource-cobol
docker run --rm -it -v `pwd`/src:/oscobol/src:ro --name oscobol opensourcecobol/opensource-cobol
```

in docker container

```
cobc src/HELLO.cbl
cobcrun HELLO
```

display your console `HELLO WORLD!`

When you want stop container, follow command:

```
docker stop oscobol
```

Copyright 2019, Tokyo System House Co., Ltd. <opencobol@tsh-world.co.jp>
