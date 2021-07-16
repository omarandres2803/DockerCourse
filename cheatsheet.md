# Docker CheatSheet

## Run a container
> docker run hello-world

---

## Run a container but giving it another name
> docker run --name hello-platzi hello-world

---

## Rename an existing container
> docker rename hello-platzi hola-platzi

---

## See the details of a container
> docker inspect \<container ID\>

---

## List containers
> docker ps

---

## List all the containers
> docker ps -a

---

## Remove a container
> docker rm hello-world

---

## Remove all the stopped containers
> docker container prune

---

## Run container in interactive mode
> docker run -it ubuntu

---

## Run Image, detach it and specify a command to be executed
> docker run -d ubuntu tail -f /dev/null

---

## Execute a command on an existing and running container
> docker exec -it \<container name\> bash

---

## To stop a container
> docker stop \<container name\>

---

## Expose the container (Redirecting container ports to host ports)
> docker run --name \<name\> -p \<host_port:container_port> \<container_name\>

--- 

## Get logs of a running container
> docker logs \<container_name>

---

## Follow logs of a running container
> docker logs -f \<container_name>

---

## See the last n lines of logs 
> docker logs --tail \<n_lines> -f \<container_name>

---

## Delete all the containers (those stopped and also those running)
> docker rm -f $(docker ps -aq)

---

## Clean system from stopped containers, not used images, volumes and networks
> docker system prune

---

## Bind mounts (To link a host's folder with a container's folder)
> docker run -d -v \<host_folder>:\<container_folder> \<container_name>

---

# Volumes

## List all volumes
> docker volume ls

---

## Create a volume
> docker volume create \<volume_name>

---

## Associate a volume to a container
> docker run --mount src=\<name_of_volume>,dst=\<container_destination_folder> \<container_name>

---

# Insert and Extract files to/from a container

## Copy a file/folder to a container's folder
> docker cp \<file_name> \<container_name>:\<container_folder>

---

## Copy a file/folder from a container
> docker cp \<container_name>:\<container_folder> \<host_destination_folder>

--- 

# Images

## See an image history
> docker history \<image>

---

## List all images
> docker image ls

---

## Pull an image (from docker hub by default)
> docker pull \<image_name>:\<version>

---

## Build an Image from a docker file
> docker build -t \<image_name>:\<version_name> \<build_context> 

The docker build context is where the docker file is located.

---

## Rename your image, change the tag
> docker tag \<old_image_name>:\<old_image_tag> \<new_image_name>:\<new_image_tag> 

---

## Publish an image to your docker hub repo

* First you have to log in to your docker hub account:
> docker login

* Then you push your image (it has to have the name of your repo and not the name of ubuntu's repo, for example)
> docker push \<image_name>

---

# Docker Networks

## See network list
> docker network ls

---

## Create a network
> docker network create \<network_name>

To specify that we want containers to be able to connect to it, we would have to add the --attachable flag:

> docker network create --attachable \<network_name>

---

## See details of a network
> docker network inspect \<network_name>

---

## Connect a container to a network
> docker network connect \<network_name> \<container_name>

---

# Docker Compose

## To put the environment up
> docker-compose up

> docker-compose up -d

> docker-compose ps

---

## To execute a command on a container of our docker-compose, we have to communicate with the service like this :
> docker-compose exec \<service_name> <\command>

---

## To destroy the environment and clean
> docker-compose down