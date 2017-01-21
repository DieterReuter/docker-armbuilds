# docker-armbuilds

This repo contains Docker Engine .deb Debian packages I've built for Debian-Jessie OS running on aarch64 architectures, since these packages are currently not available from the upstream docker/docker project.

DISCLAMER: Use it at your own risk. ;-)


## Build instructions
In order to build a Debian package for the Docker Engine you can easily build it with the following commands:
```
$ git clone https://github.com/docker/docker
$ git checkout v1.13.0
$ make deb
```
This will build all the defined .deb packages for the current architecture. On a [packet.net Cloud Server](https://www.packet.net) Type 2A machine running Ubuntu 16.04, which is a 96-core 128GByte ARMv8 server based upon Cavium ThunderX CPUs, this will build `aarch64` aka `arm64` packages of the Docker Engine.

Usually you just want to build a single .deb package which can be done with the following command:
```
$ DOCKER_BUILD_PKGS="debian-jessie" make deb
```


## License

MIT - see the [LICENSE](./LICENSE) file for details.
