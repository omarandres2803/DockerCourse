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