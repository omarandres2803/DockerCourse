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
