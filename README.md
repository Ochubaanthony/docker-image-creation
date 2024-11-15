# docker-image-creation
How to build  From the Docker file you can build the Docker Image


GO TO THE UBUNTU VM CREATED 
sudo apt update && sudo apt upgrade -y
run docker                        you noticed no docker was installed
sudo snap install docker
sudo chmod 666 /var/run/docker.sock
docker

docker ps
nano Dockerfile 
FROM ubuntu:latest
LABEL maintainer="ochubanthony@gmail.com"

RUN apt-get update && \
    apt-get install -y \
    curl \
    wget \
    vim \
    git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
WORKDIR /Anthony

CMD ["echo", "hello, Anthony welcomes you to docker!"]

docker build -t anthonyubuntu .
docker image ls
docker run anthonyubuntu
