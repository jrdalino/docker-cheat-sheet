# docker-cheat-sheet

## Install
- https://docs.docker.com/docker-for-mac/install/

## Dockerfile
- Install Maven

```
FROM openjdk:8-jdk-alpine
COPY target/book-service-0.1.0.jar app.jar
ENTRYPOINT ["java","-jar","/app.jar"]
```

## Build
- Build an image from the Dockerfile in the current directory and tag the image
```
$ docker build -t myimage:1.0 .
```

- List all images that are locally stored with the Docker Engine
```
$ docker image ls
```

- Delete an image from the local image store
```
$ docker image rm myimage:1.0
```

## Share
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

## Run
- Run a container
```
$ docker run --name mycontainer -p 5000:80 myimage:1.0
```

- List all containers
```
$ docker container ls --all
```

- Stop a running container using SIGTERM or SIGKILL
```
$ docker container stop mycontainer
$ docker container kill mycontainer
```

- Remove a container
```
$ docker container rm mycontainer
```

- Print the last 100 lines of a container's logs
```
docker container logs --tail 100 mycontainer
```

- List the networks
```
$ docker network ls
```
