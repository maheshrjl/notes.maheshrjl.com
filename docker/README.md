# 🚀 Docker

`docker version` - Docker client/engine version

`docker info` - Show docker engine configuration (info about containers & images)

### Docker CLI structure

* Old: `docker <command> (options)`
* New: `docker <command> <sub-command> (options)`

### Isolation mode for windows containers

* `process isolation`: multiple container instances run concurrently on a given host sharing the same kernel with the host as well as each other. Same as how Linux containers run.
* `Hyper-V isolation`: Offers enhanced security and broader compatibility between host and container versions. With Hyper-V isolation, multiple container instances run concurrently on a host; however, each container runs inside of a highly optimized virtual machine and effectively gets its own kernel. The presence of the virtual machine provides hardware-level isolation between each container as well as the container host.

### Shell Inside a Container

`docker exec -it <container name> /bin/bash` execute a bash shell in the container

docker exec -it \<container name> \<command> - execute any command inside the container

#### Check Running Containers <a href="#check-running-containers" id="check-running-containers"></a>

`docker ps` - show running container&#x20;

#### SSH Into Container

* `docker exec -it <container name> /bin/sh` - SSH into a container

#### Restart A Container

* docker restart \<container name>

#### Check CPU and Memory Usage

* `docker stats` - Display a live stream of running containers usage statistics.
* `docker system df` - Display information about disk space being used by your containers.

### Container Management

#### Starting docker containers

```
docker container run --publish 80:80 --detach --name webserver nginx
```

Start existing container: `docker container start -ai <name> <command>`

{% hint style="info" %}
Container run as long as the command that was executed on startup runs. Eg: If bash shell was executed on startup, the container will stop when the shell is terminated.
{% endhint %}

#### List containers

List running containers: `docker container ls`

List all containers: `docker container ls -a`

#### Viewing Logs

* View Logs for a container: `docker container logs name`
* Follow container logs: `docker container logs name -f`
* View logs help: `docker container logs --help`

#### Container config info & utilization:

* View processes running inside a container: `docker container top`
* details of container config: `docker container inspect name`
* performance stats of containers(stream): `docker container stats`
* `docker system df` - Display information about disk space being used by your containers.

#### Getting a shell inside a container

* `docker container run -it` - Start a new container interactively (container will stop when the shell/command is terminated)
* `docker container exec -it` - Run a command inside exisiting container

#### Docker Cleanup

* To clean an unused/dangling image: `Docker image prune`
* To remove an image that is not used in a container: `Docker image prune -a`
* To prune the entire system: `Docker system prune`
* To kill all running containers: `Docker kill $ (docker ps -q)`
* To delete all stopped containers: `docker rm $(docker ps -a -q)`
* To delete all images: `docker rmi $(docker images -q)`

{% hint style="info" %}
A running container cannot be removed unless stopped or using `docker` container rm -f name
{% endhint %}

### Docker Images

Image contains applications binaries, dependencies for the app along with metadata about how to run it

#### Image details

* List downloaded images: `docker image ls`
* View history of image layers: `docker image history nginx:latest`
* Inspecting a docker image: `docker image inspect nginx`

#### Tagging images

* Give a new tag to a image: `docker image tag <source-img:tag> <taget-image:tag>`

#### Uploading images

* Upload image to docker hub: `docker image push <img-name>`

#### Cleaning up images

* Clean up dangling images: `docker image prune`
* Clean all images that are not in use: `docker image prune -a`
* Clean up everything: `docker system prune`

### Docker Networking

#### Basic docker Networking commands

* Show networks: `docker network ls`
* Inspect a network: `docker network inspect`
* Create a network: `docker network create --driver`
* Attach a network to a container: `docker network connect`
* Detach a network from container: `docker network disconnect`
