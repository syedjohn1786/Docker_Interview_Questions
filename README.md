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
==========
docker build -t myapp:v1 .

In this example, the Dockerfile should be named "Dockerfile" and located in the current directory. If your Dockerfile has a different name or is located in a different directory, you would specify the appropriate path in place of the dot (.).

4). What is a docker hub ?
Docker Hub is a cloud-based registry where developers can find and share Docker images. Users can also create and store their custom images on Docker Hub.

5). What is docker compose ?
Docker Compose is a tool for defining and managing multi-container applications. It allows you to define complex applications consisting of multiple interconnected containers using a single configuration file.

















