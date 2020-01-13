# docker-cheat-sheet

## Install
- https://docs.docker.com/docker-for-mac/install/

## Dockerfile (To Follow)

## Build Images
- Build an image from the Dockerfile in the current directory and tag the image
```
$ docker build -t myimage:1.0 .
```

- List all images that are locally stored with the Docker Engine
```
$ docker image ls
```

- Inspect an image
```
$ docker inspect <IMAGE_ID>
```

- Delete an image from the local image store
```
$ docker image rm myimage:1.0
```

## Share Images
- Push an image from a registry
```
$ docker push <AWS_ACCOUNT_ID>.dkr.ecr.ap-southeast-1.amazonaws.com/myimage:2.0
```

- Tag a local image with new image name and tag
```
$ docker tag myimage:1.0 <AWS_ACCOUNT_ID>.dkr.ecr.ap-southeast-1.amazonaws.com/myimage:2.0
```

- Pull an image from a registry
```
$ docker pull myimage:2.0
```

## Run Containers
- Run a container
```
$ docker run --name mycontainer -p 5000:80 myimage:1.0
```

- List all containers
```
$ docker container ls
$ docker ps
```

- Inspect a containers
```
$ docker inspect <CONTAINER_ID_OR_NAME>
```

- Streat data from container
```
$ docker stats <CONTAINER_ID_OR_NAME>
```

- Print the last 100 lines of a container's logs
```
docker logs --tail 100 <CONTAINER_ID_OR_NAME>
```

- Restart a container
```
$ docker restart <CONTAINER_ID_OR_NAME>
$ docker stop <CONTAINER_ID_OR_NAME>
$ docker start <CONTAINER_NAME>
```

- Kill a running container
```
$ docker kill <CONTAINER_ID_OR_NAME>
```

- Remove a container
```
$ docker rm <CONTAINER_ID>
```

## Networking
- List the networks
```
$ docker network ls
```

- Inspect a network
```
$ docker network inspect <NETWORK_ID>
```
