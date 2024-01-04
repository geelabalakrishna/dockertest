=======================================================================================================================
2-docker-remove-dangling-images

FROM ubuntu:20.04

ENTRYPOINT ["echo", "Hello World"]


docker build -t hello:v1



FROM rockylinux:8

ENTRYPOINT ["echo", "Hello World"]


docker build -t hello:v1



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
