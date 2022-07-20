# 🚀 Docker

### Getting a Shell Inside a Container

`docker exec -it <container name> /bin/bash` execute a bash shell in the container

docker exec -it \<container name> \<command> - execute any command inside the container



### Check Running Containers <a href="#check-running-containers" id="check-running-containers"></a>

`docker ps` - show running container&#x20;



### SSH Into Container

* `docker exec -it <container name> /bin/sh` - SSH into a container



### Restart A Container

* docker restart \<container name>



### Check CPU and Memory Usage

* `docker stats` - Display a live stream of running containers usage statistics.
* `docker system df` - Display information about disk space being used by your containers.
