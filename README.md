# Docker_Interview_Questions
1). What is Docker ?
Docker is an open source containerization platform which enables developers to package applications into containers and manage the lifecycle of containers.

2). What are containers ?
Containers are lightweight software packages which encapsulates Application code, libraries, system dependencies, runtime environment into a single unit.
Containers provide an isolated environment for applications to run, ensuring that they behave the same way across various development, testing, and production environments.

3). What is a docker image ?
A Docker image is a read-only template used to create containers. Images contain the application code, runtime, system tools, libraries, and settings required for the application to run.
Images are created from a Dockerfile, which is a script that has instructions to build the image.

Syntax to create an image from the dockerfile
=============================================
docker build -t <image_name>:<tag> <path_to_dockerfile_directory>

docker build: This is the command to build a Docker image.

-t <image_name>:<tag>: This option allows you to specify a name and an optional tag for the image you're creating.
For example, myapp:latest would be the image name "myapp" with the tag "latest."

<path_to_dockerfile_directory>: This is the path to the directory where your Dockerfile is located. Docker will use the Dockerfile to build the image.

Example :
=============

docker build -t myapp:v1 .

In this example, the Dockerfile should be named "Dockerfile" and located in the current directory. If your Dockerfile has a different name or is located in a different directory, you would specify the appropriate path in place of the dot (.).

4). What is a docker hub ?
Docker Hub is a cloud-based registry where developers can find and share Docker images. Users can also create and store their custom images on Docker Hub.

5). What is docker compose ?
Docker Compose is a tool for defining and managing multi-container applications. It allows you to define complex applications consisting of multiple interconnected containers using a single configuration file.

6). What is docker swarm and kuberntes ?
Docker Swarm and Kubernetes are container orchestration platforms that help manage the deployment, scaling, and management of containers across clusters of machines. They provide features like load balancing, automatic scaling, service discovery, and more.

7). How containers are different from virtual machines ?
========================================================
Containers are lightweight in nature because they dont have complete OS , they depends and share on the host OS.
Virtual machines have their own complete OS.
As we know OS is heavy in size and due to complete OS in virtual machines, the image size is very large . Since containers dont have complete OS , the image size in containers are low comapred to image size in virtual machines.

8). What is docker lifecycle ?
=======================================================
In simple words, the docker lifecycle is as below :

DockerFile ---> Docker Image ---> Docker Container

DockerFile consists of some instructions or commands required to build an image (For example base image, dependencies/Libraries required to run an application etc)
Once the image is created, you can run some docker commands to create  docker container.
Finally, you can push docker image to a docker registry like DockerHub, AWS ECR etc.

Commands :
==========
docker build: Builds an image from a Dockerfile.
docker images: Lists the images available on the host.
docker push: Pushes an image to a registry.
docker pull: Downloads an image from a registry.
docker run: Creates and starts a new container from an image.
docker ps: Lists running containers.
docker ps -a: Lists all containers (running and stopped).
docker inspect: Displays detailed information about a container.
docker start: Starts a stopped container.
docker stop: Stops a running container.
docker restart: Stops and then starts a container.
docker pause: Pauses a running container.
docker unpause: Unpauses a paused container.
docker rm: Removes one or more stopped containers.
docker exec: Runs a command inside a running container.
docker logs: Fetches the logs of a container.

9). What are the different docker components ?
=======================================================
1. Client (Docker CLI)   2. Docker Host (Docker Daemon)   3. Docker registry

   We will execute the commands like docker build, docker run through docker CLI
   Docker Daemon is the heart of docker, daemon receives the request when we give command like docker build.
   Once daemon goes down, entire docker will be down. So daemon is the one who receives and executes the actions from the client.
   (sudo systemctl stop docker) command used to stop docker daemon.

10). What is the difference between docker COPY and docker ADD ?
======================================================================
Docker COPY : The COPY command is used to copy files and directories from the host machine to the image.
Syntax :  COPY <src> <dest>
<src> can be a file or a directory on the host, and <dest> is the destination directory inside the image.
COPY is straightforward and doesn't perform any automatic extraction or downloading.
It's generally recommended to use COPY for copying local files into the image.

Example :
=========
COPY app-files /app


Docker ADD : The ADD command is also used to copy files and directories from the host machine to the image.
Syntax : ADD <src> <dest>
In addition to simple copying, ADD has additional features:
It can automatically extract compressed files (like tarballs) into the destination directory.
It can also download files from URLs and copy them to the image.

Example :
===========
ADD app-files.tar.gz /app

11). What is the difference between CMD and Entrypoint in docker ?





















