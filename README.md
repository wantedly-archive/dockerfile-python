# Python for Ubuntu [![](https://quay.io/repository/wantedly/python/status)](https://quay.io/repository/wantedly/python)
This Dockerfile is ported from debian's official python image to Ubuntu.
For more information about this, please see [official one's README](https://github.com/docker-library/python).

![](https://raw.githubusercontent.com/docker-library/docs/master/python/logo.png)

## SUPPORTED TAGS

* [`2.7.9`](2.7/Dockerfile)

## HOW TO USE
Create a `Dockerfile` in your Python app project

```
FROM quay.io/wantedly/python:2.7
CMD ["./your-daemon-or-script.py"]
```

## HOW TO DEVELOP
clone repo and bootstrapping.

```bash
# on your local machine
$ git clone https://github.com/wantedly/dockerfile-python.git && cd dockerfile-python
$ script/bootstrap
```

set some configuration

```bash
# .env
TIMEZONE=Asia/Tokyo
```

start CoreOS VM

```bash
$ vagrant up
```

edit some code

```bash
$ vi Dockerfile
```

login to CoreOS VM and build it
```
$ vagrant ssh
@core-01 $ cd share
@core-01 $ docker build -t target .
@core-01 $ script/test
```

## LICENSE
[![MIT License](http://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE)
