# Containers
## Lifecycle
`docker run` creates and starts a container in one command

`docker rm` deletes a container

`docker rm $(docker ps -aq)` removes all docker containers

## Starting & Stopping
`docker start` starts a container

`docker stop` stops a running container

`docker stop $(docker ps -aq)` stops all running containers

## Info
`docker ps` shows running containers

`docker ps -a` shows running and stopped containers

`docker stats` shows container's resource usage stats

`docker diff` shows changed files in the container's file system

## Executing Commands
`docker exec` to execute a command in a container


# Images
## Lifecycle
`docker images` shows all images

`docker build (--tag={tag})` creates image from Dockerfile

`docker rmi` removes an image

`docker rmi $(docker images -q)` remove all images

## Info
`docker history` shows history of an image

`docker tag` tags an image to a name

