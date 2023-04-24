# Learn k8s

## Overview

- What is Kubernetes?

- K8s Architecture

- Main K8s Components

- Minikube and Kubectl - Local Setup

- Main Kubectl Commands - K8s CLI

- K8s YAML Configuration File

- Hands-On Demo

-- 

- K8s Namspaces - Organize Your Components

- K8s Ingress

- Helm - Package Manager

- Volumes - Persisting Data in K8s

- K8s StatefulSet - Deploying Stateful Apps

- K8s Services

## What is Kubernetes?

- Definition (Open source `container orchestration tool`, developed by google, manage containerized applications in different deployment environments)

- From Monolith to Microservices

- High availability (no downtime)

- Scalability

- Disaster recovery (backup and restore)

## K8s Components

### Pod

- Smallest unit of K8s

- Abstraction over container

- Usually 1 application per Pod

- Each Pod gets its own IP address

- New IP address on re-creation

### Service and Ingress (External / Internal service)

- Permanent IP address

- Lifecycle of Pod and Service Not connected

- Load balancer

### ConfigMap

- External configuration of your application

- **Dont put credentials into ConfigMap**

### Secret (like env)

- Used to store secret data

- base64 encoded

- **The built-in security mechanism is not enabled by default**

### Volumes

- Remote (K8s Cluster), local storage (local machine)

### Deployment

- blueprint for *app pods

- Abstraction of pods

- DB can't be replicated via deployment

### StatfulSet (not easy)

- DB are often hosted outside of K8s cluster

## K8s architecture

### Worker machine in K8s cluster

- each Node has multile Pods on it

- 3 process must be installed on every Node (Container runtime, kube proxy, kubelet)

- Worker Nodes do the actual works

### Master process

- 4 processes run on every master node

- Api Server:
  - Cluster gateway
  - Acts as a gatekeeper for authentication
  - Validates requests
- Scheduler
- Controller manager
- etcd:
  - Cluster brain
  - Cluster changes get stored in the key value store

## Example Cluster Setup

- 2 masters
- 3 nodes
- ...
