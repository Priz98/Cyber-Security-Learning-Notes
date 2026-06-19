# Docker Hands-On Labs

## Topic 01 - List Images

### Command

```bash
docker images
```

### Purpose

Displays all Docker images available on the local system.

### What I Observed

* Shows repository name
* Shows image tag
* Shows image ID
* Shows image size

## Topic 02 - Pull Image & Run Ubuntu Container

### Command

```bash
docker pull ubuntu
docker run -it ubuntu
```

### Purpose

First command pull the Ubuntu Image from Docker Hub.

Second command creates and starts an Ubuntu container and provides an interactive terminal.

### Parameters

* `-i` : Interactive mode
* `-t` : Allocate a terminal

### What I Observed

* Docker downloaded the Ubuntu image if it was not already available.
* A shell opened inside the container.

### Screenshot

![Ubuntu Container Shell](Images/Image-Pull & Create Container.png)

### What I Learned

Containers are running instances of images and provide isolated environments for applications.

---

## Lab 03 - List Containers

### Command

```bash
docker ps -a
```

### Purpose

Displays all containers, including stopped containers.

### Screenshot

![Docker PS Output](Images/docker-ps.png)

### What I Learned

Stopping a container does not delete it. Containers remain on the system until they are manually removed.

---

## Lab 04 - Execute Commands Inside Container

### Commands

```bash
pwd
whoami
hostname
mkdir test
ls
```

### Purpose

Explore the container environment and understand filesystem isolation.

### Screenshot

![Container Commands](Images/container-commands.png)

### What I Learned

* Containers have their own filesystem.
* Files created inside a container are isolated from the host system.
* The hostname often corresponds to the container ID.

---

## Overall Learning

* Images are templates used to create containers.
* Containers are running instances of images.
* Docker provides isolated environments for applications.
* Containers are lightweight compared to virtual machines.
* Docker is useful for creating cybersecurity lab environments.

```
```

