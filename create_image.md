# How to create a docker image

This process is based on the "docker file". This docker file looks like this:

```
FROM ubuntu:latest

RUN touch /usr/src/hola-platzi.txt
```

In the previous example, we can see that a docker image always starts with a FROM statement. The FROM means that the image is based on another base image.

The RUN statement gives us the opportunity to run a command, and this would be executed when the image is built.