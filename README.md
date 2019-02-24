# Docker-Commands
Few Useful Docker Commands

### To build a docker image

  * If dockerfile is present in the same directory:
    
  ```
        docker build -t <name-of-docker-image> .
 ```
    
   *[NOTE] Don't forget to put dot at the end.*

   *[NOTE] Docker enforce image name to be in lowercase.*

  * If dockerfile is present some other directory:
  
  ```
        docker build -t <name-of-docker-image> <path or url>
  ```

### To pull docker image from docker-hub

 Syntax:        docker pull <docker-image-name>

```
docker pull centos
```

### To run docker image
 
 Syntax:        docker run <docker-image-name>

```
 docker run centos
 ```
### To run an image on a particular port 
   Syntax:        docker run -p <docker-container-port>:<host-machine-port> -e <environment-variable> ref-data-app

```
docker run -p 9080:9080 -e JAVA_OPTS="-Dserver.port=9080" my-docker-image
```
###  To remove:
   - all stopped containers

   - all networks not used by at least one container

   - all dangling images

   - all build cache
   
```
  docker system prune
  ```
### To remove an image
```
  docker rmi <image-name>
```
### To remove a container
```
  docker rm <container-name>
```
### To remove all images
```
docker rmi $(docker images -q)
```
### To remove all stopped containers
```
  docker container prune
```
### To stop a container
```
 docker stop <container-id>
  ```
### To save a docker image as a tar file:
```
docker save -o <save image to path> <image name>
```
### To load the image into docker: 
```
docker load -i <path to image tar file
```
