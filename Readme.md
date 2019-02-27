# Docker and Kubernetes 101

---

# Virtual machines

---

# Linux OS and kernel

---

# Cgroups 

- CPU
- memory
- disk I/O
- network 

---

# Namespaces

- PID
- NIC (network interface )
- UID/GID
- Mounts
- UTS (hostname)

---

# Docker Engine 

- docker daemon
- docker CLI
- [Docker engine documentation](https://docs.docker.com/engine/docker-overview/)

---

# Docker Images and containers

---

# Image

- Container template
- Often based on another image
- Dockerfile used to create image (buildscript)
- Each instruction in a Dockerfile is a layer

---

# Exercise 1

- Create Apache httpd image using Dockerfile
- Serving web content from inside image
- [http://tinyurl.com/dockerfilehttpd](http://tinyurl.com/dockerfilehttpd)

---

# Java

Several tools exist for packaging java app as docker image

- [fabric8io/openshift maven plugin](https://github.com/fabric8io/docker-maven-plugin) 
- [spotify maven plugin](https://github.com/spotify/docker-maven-plugin)
- [google jib maven plugin](https://github.com/GoogleContainerTools/jib/tree/master/jib-maven-plugin)

---

# Dockerhub

- Image registry compararble to Maven central 
- Other registries exist, also private ones

---

# Exercise 2

- Serve content from local dir using Apache httpd
- How can container access content from host?
- [https://hub.docker.com/_/httpd](https://hub.docker.com/_/httpd)

---

# Exercise 3

- Run _nmap_ (network scan) against your favourite web site
- [https://hub.docker.com/r/uzyexe/nmap](https://hub.docker.com/r/uzyexe/nmap)

---

# Docker official images

- Make sure you evaluate images properly!
- _Official images_ are **curated**
	+ Base os
	+ Programming language runtimes
	+ Popular software (nginx, httpd, etc)
- Other images are **not curated**

---

# Tags

- Versions
- latest is a name used by convention
	+ typically refers to last stable version
- Tags are not necessarily _final_

---

# Docker cli

- run
- attach
- exec 
- start 
- stop
- kill

---

# Demo

    docker run -it ubuntu bash 

---


# Docker compose

Compose is a tool for defining and running multi-container Docker applications.

- Great for running apps locally
- Can be used with Docker swarm (Kubernetes alternative)

---

# Exercise 4

- Run PostgreSQL database and admin interface using _docker-compose_ 
- [https://hub.docker.com/_/postgres](https://hub.docker.com/_/postgres)

---

# Container orchestration

A standard way to deploy, run and scale containers

- Docker Swarm
- Hashicorp Nomad
- Kubernetes

---

# Kubernetes

- _de facto_ standard for running containers at scale
- Public Cloud: GKE, AKS, EKS, ...
- Private Cloud: open shift, rancher, suse, ...

---

# Key concepts (objects)

- Pods
- Service
- Deployment
- Secret/ConfigMap
- Ingress

---

# Kubernetes API

Kubernetes provides a REST api to which you can upload objects using yaml syntax

- [Deployment](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/#creating-a-deployment) 

---

# Exercise

Run Kubernetes locally using minikube, and deploy app to it

[https://kubernetes.io/docs/tutorials/hello-minikube/](https://kubernetes.io/docs/tutorials/hello-minikube/)
