# Runner images

Following images are based on official `ubuntu:20.04` image and optimized for network environment (with configured mirrors) in mainland China.

## `hanlinyang/ubuntu`

Based on official `ubuntu:20.04` image, with following tools installed from Ubuntu official repository:

- curl
- wget
- git

This image has two identical tags `latest` and `20.04`, both configured [Tsinghua mirror](https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu/) for `apt` tools.

## `hanlinyang/openjdk`

Based on `hanlinyang/ubuntu:20.04`.

Tags:

- `11`: [AdoptOpenJDK](https://adoptopenjdk.net/) 11 LTS Hotspot from AdoptOpenJDK repository, Maven from Ubuntu repository
- `latest`: identical to `11`

Maven is configured to use [Aliyun Maven repository mirrors](https://maven.aliyun.com/mvn/guide).

## `hanlinyang/node`

Based on `hanlinyang/ubuntu:20.04`.

Tags:

- `14`: [NodeSource Node.js](https://github.com/nodesource/distributions) 14 LTS with NPM, Yarn installed with NPM, CNPM installed with NPM
- `latest`: identical to `14`

NPM and Yarn are configured to use [Taobao NPM mirror](https://developer.aliyun.com/mirror/NPM).

## `hanlinyang/python`

Based on `hanlinyang/ubuntu:20.04`.

Tags:

- `3.8`: Python 3.8 from Ubuntu repository (available as `python3` and `python`), Pip from Ubuntu repository (available as `pip3` and `pip`), **no Python 2 is included**
- `latest`: identical with `3.8`

Pip is configured to use [Tsinghua PyPI mirror](https://mirrors.tuna.tsinghua.edu.cn/help/pypi/).
