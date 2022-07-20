# Docker Info

### Docker version, docker client & docker server information

#### Docker client/engine version

```
docker version
```

#### Docker engine configs

Shows information about containers & images as well

```
docker info
```

### Docker CLI structure

* Old: `docker <command> (options)`
* New: `docker <command> <sub-command> (options)`

### Isolation mode for windows containers

* `process isolation`: multiple container instances run concurrently on a given host sharing the same kernel with the host as well as each other. Same as how Linux containers run.
* `Hyper-V isolation`: Offers enhanced security and broader compatibility between host and container versions. With Hyper-V isolation, multiple container instances run concurrently on a host; however, each container runs inside of a highly optimized virtual machine and effectively gets its own kernel. The presence of the virtual machine provides hardware-level isolation between each container as well as the container host.
