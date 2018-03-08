# hopper-docker

[![Build Status](https://travis-ci.org/ps1337/hopper-docker.png?branch=master)](https://travis-ci.org/ps1337/hopper-docker)

A dockerized version of the reverse engineering tool hopper (hopperapp.com). Run `make` for more info.


Running can be as simple as

```
xhost +local:root && \
sudo docker run \
-d \
--name $(CONTAINER_NAME) \
-e DISPLAY=$DISPLAY \
--cap-add=SYS_PTRACE \
-v /tmp/.X11-unix:/tmp/.X11-unix:ro \
-v $PWD/sharedFolder:/var/sharedFolder \
bananafett/hopper-docker:latest
```

Check the Makefile for further info.
