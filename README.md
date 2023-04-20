# Day - 1: Docker - https://youtu.be/3c-iBn73dDE

## Overview

1. What is docker? What is a Container?

2. Docker vs. Virtual Machine

3. Docker installation

4. Main commands

5. Debugging a Container

6. Developing with Containers

7. Docker Compose - Running multiple services

8. Dockerfile - Building own Docker image

9. Private Docker Repository (AWS)

10. Deploying the containerized App

11. Volumes - Persiting Data

12. Volumes demo

## 1. What is Container

### What

- package, necessary dependencies and configuration
- portable artifact, shared and moved
- develop and deploy, more efficient

- Container is made of **images** (linux image layer, ..., application image layer)

### Where

- Container repository (https://hub.docker.com/)  

### How it helps

- Before containers: 
  New projects -> install serivices (PostgresSQL, Redis, Node, ...) -> Many steps, version, OS

- After containers:
  New projects -> install isolated environment, packaged with all needed configuration -> one command for one service

### Note

- Different between container and image
- CONTAINER Port vs HOST port

### Basic commands

- `docker pull` (version tag) 
- `docker run` (-d, :version, -p)
- `docker start`
- `docker stop`
- `docker ps` (-a)
- `docker exec -it` (/bin/bash) (ls, cd, pwd, env, exit)
- `docker logs`