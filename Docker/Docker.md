### Docker Docs 
https://docs.docker.com/reference/cli/docker/

### Useful docker commands

* docker images -> list all images available
* docker pull <IMAGE> -> fetch image
* docker run <IMAGE> -> creates and start container in attached mode (pulls and starts container)
* docker run -d <IMAGE> -> start container in detached mode
* docker stop <CONTAINER_ID>
* docker start <CONTAINER_ID>
* docker ps -> list running containers
* docker ps -a -> list bith running and stopped containters
* docker run -p<HOST_PORT>:<CONTAINER_PORT> <IMAGE> (You can bind ports with -p or -e for a environment variable)
* docker run --name <NAME> <IMAGE> (You can name containers with --name)
* docker logs <CONTAINER_ID>(Show log)
* docker logs <CONTAINER_NAME> (Show log)
* docker logs <CONTAINER_NAME> | tail (only show last logs)
* docker logs <CONTAINER_NAME> -f (stream logs)
* docker exec -it <CONTAINER_ID> sh (Enter container with terminal)
* docker exec -u 0 -it <CONTAINER_ID> sh (Add -u 0 to enter container as root user)
* docker network ls (check existing networks)
* docker network create <NAME> (create new network)
* docker build -t <IMG_NAME>:<VERSION_TAG> . (build image)
* docker rm <CONTAINER_ID> (Delete container)
* docker rmi <IMAGE_ID> (Delete image)

### Docker Compose

Run multiple Docker containers with one command.
Create in combination with docker swarm with docker swarm you can use docker compose up and services to run multiple
containers.

* docker-compose -f <FILE_NAME> up
* docker-compose -f <FILE_NAME> down


### Dockerfile example

```dockerfile
Dockerfile -> blueprint for building images
FROM (image based on)
ENV
RUN (executes linux cmd in container)
COPY (runs on host)
CMD (entry point cmd, so only one)
```
