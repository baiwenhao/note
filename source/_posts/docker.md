---
title: docker
abbrlink: f255ffad
date: 2017-07-24 15:08:20
tags:
---

## 基本命令
docker info
docker images
docker ps -l || -a
docker version
docker stop id
docker start id
docker rmi id
docker rm name
docker search name
docker pull name

## mongodb
Status: Downloaded newer image for mongo:latest (下载成功)
docker run -d -v /var/lib/mongo:/data/db -v /home/user/mongo.conf:/etc/mongo.conf -p port:port image_name

docker run -p 27017:27017 -v /Users/baiwenhao/workSpace/mongodb/data:/data -d mongo 
docker run -p 27017:27017 -v /c/Users/Administrator/Desktop/mongodb/data:/data -d mongo 

-p 27017:27017 将容器的27017 端口映射到主机的27017 端口
-v $PWD/db:/data/db 将主机中当前目录下的db挂载到容器的/data/db，作为mongo数据存储目录

## 镜像加速
容器镜像服务 => 镜像加速器 （我的加速地址） https://k454h3he.mirror.aliyuncs.com
docker的配置中找到daemon => registry mirrors (添加地址) => apply

参考
https://docs.docker.com/samples/library/mongo/#shared-tags
