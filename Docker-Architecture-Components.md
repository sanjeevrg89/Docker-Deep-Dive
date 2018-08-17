Docker Architecture:
====================

![Docker Architecture](https://github.com/devops2201/Docker-Deep-Dive/blob/master/Dockercomponents.png)

* Docker uses a client-server architecture
* Docker client talks to the Docker daemon, which does the heavy lifting of building, running, and distributing your Docker containers
* Docker client and daemon can run on the same system, or you can connect a Docker client to a remote Docker daemon
* Docker client and daemon communicate using a REST API, over UNIX sockets or a network interface

Docker Engine:
--------------
* Docker Engine is a client-server application with the following components:
1. A server which is a type of long-running program called a daemon process (the dockerd command)
2. A REST API which specifies interfaces that programs can use to talk to the daemon and instruct it what to do
3. A command line interface (CLI) client (the docker command)

![Docker Engine](https://github.com/devops2201/Docker-Deep-Dive/blob/master/Dockerengine.png)


Docker Components:
------------------

* Docker Daemon
* Docker Client
* Docker.io Registry

Docker Daemon:
--------------
* Docker daemon (dockerd) listens for Docker API requests and manages Docker objects such as images, containers, networks, and volumes
* A daemon can also communicate with other daemons to manage Docker services

Docker Client:
--------------
* Docker client (docker) is the primary way that many Docker users interact with Docker
* Docker client  sends commands to daemon (dockerd), which carries them out
* docker command uses the Docker API
* Docker client can communicate with more than one daemon

Docker Registry:
----------------
* Docker registry stores Docker images
* Docker Hub and Docker Cloud are public registries that anyone can use, and Docker is configured to look for images on Docker Hub by default
* Docker Hub -> https://hub.docker.com/
* You can run your own private registry
