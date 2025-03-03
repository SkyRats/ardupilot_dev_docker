# ArduPilot CI Containers

Contains Dockerfiles for Docker CI containers to build and test ArduPilot on CI systems like GitHub Action.
For daily development, you can use the dockerfile provide into ArduPilot directory, see https://ardupilot.org/dev/docs/building-setup-linux.html#id1

## Container Hierarchy

### Docker Images

The docker images provide base environment to compile ArduPilot. They don't contain ArduPilot code but only the packages needed to compile the binaries. Each image is based on Ubuntu 20.04 or 22.04.

The main image is [ardupilot-dev-base ](Dockerfile_dev-base). Other images will inherit from it.
Each image is specialized to contain only the necessary tools to build the related binaries.

### Images statistics

- [ardupilot/ardupilot-dev-base](https://hub.docker.com/r/ardupilot/ardupilot-dev-base) [![](https://images.microbadger.com/badges/image/ardupilot/ardupilot-dev-base.svg)](http://microbadger.com/images/ardupilot/ardupilot-dev-base) [![Docker Size](https://img.shields.io/docker/image-size/ardupilot/ardupilot-dev-base/latest)](https://hub.docker.com/r/ardupilot/ardupilot-dev-base) [![Docker Pulls](https://img.shields.io/docker/pulls/ardupilot/ardupilot-dev-base.svg)](https://hub.docker.com/r/ardupilot/ardupilot-dev-base)
- [ardupilot/ardupilot-dev-chibios](https://hub.docker.com/r/ardupilot/ardupilot-dev-chibios) [![](https://images.microbadger.com/badges/image/ardupilot/ardupilot-dev-chibios.svg)](http://microbadger.com/images/ardupilot/ardupilot-dev-chibios) [![Docker Size](https://img.shields.io/docker/image-size/ardupilot/ardupilot-dev-chibios/latest)](https://hub.docker.com/r/ardupilot/ardupilot-dev-chibios) [![Docker Pulls](https://img.shields.io/docker/pulls/ardupilot/ardupilot-dev-chibios.svg)](https://hub.docker.com/r/ardupilot/ardupilot-dev-chibios)
- [ardupilot/ardupilot-dev-chibios-clang](https://hub.docker.com/r/ardupilot/ardupilot-dev-chibios-clang) [![](https://images.microbadger.com/badges/image/ardupilot/ardupilot-dev-chibios-clang.svg)](http://microbadger.com/images/ardupilot/ardupilot-dev-chibios-clang) [![Docker Size](https://img.shields.io/docker/image-size/ardupilot/ardupilot-dev-chibios-clang/latest)](https://hub.docker.com/r/ardupilot/ardupilot-dev-chibios-clang) [![Docker Pulls](https://img.shields.io/docker/pulls/ardupilot/ardupilot-dev-chibios-clang.svg)](https://hub.docker.com/r/ardupilot/ardupilot-dev-chibios-clang)
- [ardupilot/ardupilot-dev-clang](https://hub.docker.com/r/ardupilot/ardupilot-dev-clang) [![](https://images.microbadger.com/badges/image/ardupilot/ardupilot-dev-clang.svg)](http://microbadger.com/images/ardupilot/ardupilot-dev-clang) [![Docker Size](https://img.shields.io/docker/image-size/ardupilot/ardupilot-dev-clang/latest)](https://hub.docker.com/r/ardupilot/ardupilot-dev-clang) [![Docker Pulls](https://img.shields.io/docker/pulls/ardupilot/ardupilot-dev-clang.svg)](https://hub.docker.com/r/ardupilot/ardupilot-dev-clang)
- [ardupilot/ardupilot-dev-armhf](https://hub.docker.com/r/ardupilot/ardupilot-dev-armhf) [![](https://images.microbadger.com/badges/image/ardupilot/ardupilot-dev-armhf.svg)](http://microbadger.com/images/ardupilot/ardupilot-dev-armhf) [![Docker Size](https://img.shields.io/docker/image-size/ardupilot/ardupilot-dev-armhf/latest)](https://hub.docker.com/r/ardupilot/ardupilot-dev-armhf) [![Docker Pulls](https://img.shields.io/docker/pulls/ardupilot/ardupilot-dev-armhf.svg)](https://hub.docker.com/r/ardupilot/ardupilot-dev-armhf)
- [ardupilot/ardupilot-dev-armhf-musl](https://hub.docker.com/r/ardupilot/ardupilot-dev-armhf-musl) [![](https://images.microbadger.com/badges/image/ardupilot/ardupilot-dev-armhf-musl.svg)](http://microbadger.com/images/ardupilot/ardupilot-dev-armhf-musl) [![Docker Size](https://img.shields.io/docker/image-size/ardupilot/ardupilot-dev-armhf-musl/latest)](https://hub.docker.com/r/ardupilot/ardupilot-dev-armhf-musl) [![Docker Pulls](https://img.shields.io/docker/pulls/ardupilot/ardupilot-dev-armhf-musl.svg)](https://hub.docker.com/r/ardupilot/ardupilot-dev-armhf-musl)
- [ardupilot/ardupilot-dev-aarch64](https://hub.docker.com/r/ardupilot/ardupilot-dev-aarch64) [![](https://images.microbadger.com/badges/image/ardupilot/ardupilot-dev-aarch64.svg)](http://microbadger.com/images/ardupilot/ardupilot-dev-aarch64) [![Docker Size](https://img.shields.io/docker/image-size/ardupilot/ardupilot-dev-aarch64/latest)](https://hub.docker.com/r/ardupilot/ardupilot-dev-aarch64) [![Docker Pulls](https://img.shields.io/docker/pulls/ardupilot/ardupilot-dev-aarch64.svg)](https://hub.docker.com/r/ardupilot/ardupilot-dev-aarch64)
- [ardupilot/ardupilot-dev-coverage](https://hub.docker.com/r/ardupilot/ardupilot-dev-coverage) [![](https://images.microbadger.com/badges/image/ardupilot/ardupilot-dev-coverage.svg)](http://microbadger.com/images/ardupilot/ardupilot-dev-coverage) [![Docker Size](https://img.shields.io/docker/image-size/ardupilot/ardupilot-dev-coverage/latest)](https://hub.docker.com/r/ardupilot/ardupilot-dev-coverage) [![Docker Pulls](https://img.shields.io/docker/pulls/ardupilot/ardupilot-dev-coverage.svg)](https://hub.docker.com/r/ardupilot/ardupilot-dev-coverage)
- [ardupilot/ardupilot-dev-periph](https://hub.docker.com/r/ardupilot/ardupilot-dev-periph) [![](https://images.microbadger.com/badges/image/ardupilot/ardupilot-dev-periph.svg)](http://microbadger.com/images/ardupilot/ardupilot-dev-periph) [![Docker Size](https://img.shields.io/docker/image-size/ardupilot/ardupilot-dev-periph/latest)](https://hub.docker.com/r/ardupilot/ardupilot-dev-periph) [![Docker Pulls](https://img.shields.io/docker/pulls/ardupilot/ardupilot-dev-periph.svg)](https://hub.docker.com/r/ardupilot/ardupilot-dev-periph)
- [ardupilot/ardupilot-dev-ros](https://hub.docker.com/r/ardupilot/ardupilot-dev-ros) [![](https://images.microbadger.com/badges/image/ardupilot/ardupilot-dev-ros.svg)](http://microbadger.com/images/ardupilot/ardupilot-dev-ros) [![Docker Size](https://img.shields.io/docker/image-size/ardupilot/ardupilot-dev-ros/latest)](https://hub.docker.com/r/ardupilot/ardupilot-dev-ros) [![Docker Pulls](https://img.shields.io/docker/pulls/ardupilot/ardupilot-dev-ros.svg)](https://hub.docker.com/r/ardupilot/ardupilot-dev-ros)


## Building

For building ros2 image:
```
cd docker
docker build -t ardupilot/ardupilot-dev-ros -f Dockerfile_dev-ros .
```

For building ros-bridge image: 
```
cd docker
docker build -t ardupilot/ardupilot-dev-ros-bridge -f Dockerfile_dev-ros-bridge .
```

## Running container

To run the ros bridge container:

```
docker run -it --name=bridge --net=host --rm ardupilot/ardupilot-dev-ros-bridge bash 
```

## Release

Docker images are build with GitHub Actions. On each PR, they are fresh build from latest source.
In order to publish them to DockerHub, we need to make a release and tag the image.

## Setting

The repo setting is quite simple, it needs GitHub Action and an account on DockerHub.
In order to be able to publish the image on DockerHub, you need to set two secrets on your repo setting :
`DOCKER_USERNAME` and `DOCKER_PASSWORD`
