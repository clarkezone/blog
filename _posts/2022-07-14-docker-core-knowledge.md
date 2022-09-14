---
title: Docker Core knowledge
author: clarkezone
date: 2022-06-26 00:34:00 +0800
categories: [Docker, Containers]
tags: [CoreKnowledge]
---
# Draft - work in progress

## Situation
There are a set of basic concepts and commands that represent the core knowledge you typically need to undertand and work with Docker and containers.  This post aims to arm you with a set of pointers and a checklist to learn the basics and get to a similar point.


### Tools
- Docker Desktop [link](https://www.docker.com/products/docker-desktop)
- VSCode [link](https://code.visualstudio.com)
- Azure CLI [link](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli)

- github account [link](TODO)
- dockerhub account [link](TODO)
- azure account [link](TODO)

- WSL with Ubuntu (optional) [link](https://ubuntu.com/wsl)
- Docker engine in wsl (optional) [link](https://docs.docker.com/engine/install/ubuntu/)
- Podman (optional) [link](https://podman.io)
- git cli (optional) [link](TODO)
- github cli (optional) [link](TODO)

### Learning Resources

- https://docs.microsoft.com/en-us/learn/modules/intro-to-docker-containers/?ns-enrollment-type=learningpath&ns-enrollment-id=learn.intro-to-kubernetes-on-azure

### Key Concepts

- Container Image - akin to a zip file for a container
- Container Registry - place to store images
  - Public - on the internet, can get artifacts without logging in
    - Docker hub [link](hub.docker.com)
    - Microsoft Artifact registry
  - Private - protected with password - you create yourself
    - Azure Container registry
    - Github container registry
- DockerFile - receipie for a docker container
- Container Instance - running instance of Image.
- Image Tags - labels used to version images in registries

Linux
- Networking ip address, listening rules (127.0.0.1 vs 0.0.0.0), ports
- Environment variables: set and read 

### Techniques / scenarios

Basic
1. Pull an nginx docker image from a public container registry using docker or podman
2. Run a local nginx container from nginx image using docker or podman
3. Build a local image from a Dockerfile using docker or podman (refernece [https://github.com/clarkezone/cloudnativeplayground/tree/main/testapps/golang/simplehttpserver](https://github.com/clarkezone/cloudnativeplayground/tree/main/testapps/golang/simplehttpserver)
4. List local images
5. Delete a local image
6. Tag a local image
7. Push a local image to a public registry (docker or ghcr)
8. List tags for an image in public registry (docker or ghcr)
9. Run a static website using nginx connecting a volume with static content and exposing ports (See *Running a basic web server* at this [link](https://www.docker.com/blog/how-to-use-the-official-nginx-docker-image/) )
10. Run a conatiner in disconnected/daemon and interactive modes
11. List running and stopped containers
12. Manually clean up stopped containers
13. Automatically clean up containers on exit

Intermediate
1. Create a private registry e.g. Azure Container Registry
2. Push an image to a private registry
3. Run a container setting environment variables
4. Docker Compose

Advanced
1. Exec into a running container
2. Override entrypoint
3. Reclaim disk space from unused images
4. Local multi-image builds
5. Building a container image as part of a CI/CD pipeline

### Commands

see my [docker](https://docs.clarkezone.dev/Docker) and [podman](https://docs.clarkezone.dev/Podman) cheetsheets for a more exhaustive list.

`docker image rm nginx`
