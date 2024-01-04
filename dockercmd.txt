=======================================================================================================================
2-docker-remove-dangling-images

FROM ubuntu:20.04

ENTRYPOINT ["echo", "Hello World"]


docker build -t hello:v1



FROM rockylinux:8

ENTRYPOINT ["echo", "Hello World"]


docker build -t hello:v1


https://docs.docker.com/engine/reference/commandline/rmi/
 1  docker image ls -a
    2  docker image ls
    3  docker pull ubuntu
    4  docker image ls
    5  docker history ubuntu:latest
    6  cd docker/
    7  ls
    8  vim Dockerfile
    9  docker build -t test:v1 .
   10  docker image ls
   11  docker build -t test:v2 .
   12  docker image ls
   13  docker image rm 174c8c134b2a
   14  docker build -t test:v2 .
   15  docker image ls
   16  docker image ls -a
   17  vim Dockerfile
   18  docker build -t test:v2 .
   19  docker image ls
   20  docker image ls -a
   21  docker build -t ubuntu:latest .
   22  docker image ls
   23  docker image ls -a
   24  docker image ls -f dangling=true
   25  vim Dockerfile
   26  docker build -t ubuntu:latest .
   27  docker image ls
   28  docker image ls -f dangling=true
   29  vim Dockerfile
   30  docker build -t ubuntu:latest .
   31  docker image ls
   32  docker image ls -f dangling=true
   33  root@ip-10-10-0-124:~/docker# docker image ls -f dangling=true
   34  REPOSITORY   TAG       IMAGE ID       CREATED         SIZE
   35  <none>       <none>    f82f22910d1c   5 minutes ago   72.8MB
   36  docker image prune
   37  root@ip-10-10-0-124:~/docker# docker image prune
   38  WARNING! This will remove all dangling images.
   39  Are you sure you want to continue? [y/N] y
   40  Deleted Images:
   41  deleted: sha256:f82f22910d1ce9e0f7224befb128b66fcbb8f702f794aeaf679b6b99cfd90c06
   42  Total reclaimed space: 0B
   43  docker image ls -a
   44  docker image  prune
   45  docker image  prune -f
   46  docker image prune -a
   47  docker image prune -a -f
   48  docker image ls
   49  docker image ls -a
   50  history



root@ip-10-10-0-124:~/docker# docker image ls -f dangling=true
REPOSITORY   TAG       IMAGE ID       CREATED         SIZE
<none>       <none>    f82f22910d1c   5 minutes ago   72.8MB


root@ip-10-10-0-124:~/docker# docker image prune
WARNING! This will remove all dangling images.
Are you sure you want to continue? [y/N] y
Deleted Images:
deleted: sha256:f82f22910d1ce9e0f7224befb128b66fcbb8f702f794aeaf679b6b99cfd90c06

Total reclaimed space: 0B


===============================================================================================================
