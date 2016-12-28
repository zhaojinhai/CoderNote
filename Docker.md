
# 一、Ubuntu安装
## 1、安装curl
```
 $ sudo apt-get update
 $ sudo apt-get install curl
 ```
## 2、获取 latest Docker package.
 ```
 $ curl -fsSL https://get.docker.com/ | sh
 $ curl -fsSL https://get.docker.com/gpg | sudo apt-key add -
 ```
## 3、检查安装
 (1) 输入 `docker version` 检查是否安装成功  
 (2) 输入 `docker run hello-world`命令
 ```sh
 $ docker run hello-world
 Unable to find image 'hello-world:latest' locally
 latest: Pulling from library/hello-world
 535020c3e8ad: Pull complete
 af340544ed62: Pull complete
 Digest: sha256:a68868bfe696c00866942e8f5ca39e3e31b79c1e50feaee4ce5e28df2f051d5c
 Status: Downloaded newer image for hello-world:latest

 Hello from Docker.
 This message shows that your installation appears to be working correctly.

 To generate this message, Docker took the following steps:
 1. The Docker Engine CLI client contacted the Docker Engine daemon.
 2. The Docker Engine daemon pulled the "hello-world" image from the Docker Hub.
 3. The Docker Engine daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker Engine daemon streamed that output to the Docker Engine CLI client, which sent it
    to your terminal.

 To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

 Share images, automate workflows, and more with a free Docker Hub account:
 https://hub.docker.com

 For more examples and ideas, visit:
 https://docs.docker.com/userguide/
 ```
 3.运行`docker ps -a` 显示容器
 
 ```sh
 $ docker ps -a
 CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                      PORTS               NAMES
 592376ff3eb8        hello-world         "/hello"            25 seconds ago      Exited (0) 24 seconds ago                       prickly_wozniak
 ```