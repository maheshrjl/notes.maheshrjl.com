# Docker Images

Image contains applications binaries, dependencies for the app along with metadata about how to run it

### Image details

* List downloaded images: `docker image ls`
* View history of image layers: `docker image history nginx:latest`
* Inspecting a docker image: `docker image inspect nginx`

### Tagging images

* Give a new tag to a image: `docker image tag <source-img:tag> <taget-image:tag>`

### Uploading images

* Upload image to docker hub: `docker image push <img-name>`

### Cleaning up images

* Clean up dangling images: `docker image prune`
* Clean all images that are not in use: `docker image prune -a`
* Clean up everything: `docker system prune`
