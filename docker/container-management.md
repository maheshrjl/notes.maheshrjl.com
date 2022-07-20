# Container Management

#### Starting docker containers

```
docker container run --publish 80:80 --detach --name webserver nginx
```

Start existing container: `docker container start -ai <name> <command>`

{% hint style="info" %}
Container run as long as the command that was executed on startup runs. Eg: If bash shell was executed on startup, the container will stop when the shell is terminated.
{% endhint %}

### List containers

List running containers: `docker container ls`

List all containers: `docker container ls -a`

### Viewing Logs

* View Logs for a container: `docker container logs name`
* Follow container logs: `docker container logs name -f`
* View logs help: `docker container logs --help`

### Container config info & utilization:

* View processes running inside a container: `docker container top`
* details of container config: `docker container inspect name`
* performance stats of containers(stream): `docker container stats`

### Getting a shell inside a container

* Start a new container interactively (ontainer will stop when the shell/command is terminated): `docker container run -it`
* Run a command inside exisiting container: `docker container exec -it`

### Cleanup

* To clean an unused/dangling image: `Docker image prune`
* To remove an image that is not used in a container: `Docker image prune -a`
* To prune the entire system: `Docker system prune`
* To kill all running containers: `Docker kill $ (docker ps -q)`
* To delete all stopped containers: `docker rm $(docker ps -a -q)`
* To delete all images: `docker rmi $(docker images -q)`

{% hint style="info" %}
A running container cannot be removed unless stopped or using `docker container rm -f name`
{% endhint %}
