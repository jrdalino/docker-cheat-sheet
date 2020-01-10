# docker-cheat-sheet

## Install
- https://docs.docker.com/docker-for-mac/install/

## Dockerfile
```
$ FROM openjdk:8-jdk-alpine
$ COPY target/book-service-0.1.0.jar app.jar
$ ENTRYPOINT ["java","-jar","/app.jar"]
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
$ docker image rm alpine:3.4
```

## Share
-
```
$ 
```

## Run
-
```
$ 
```

