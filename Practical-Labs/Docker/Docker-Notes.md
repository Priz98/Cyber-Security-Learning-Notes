# Docker Notes

## What is Docker?

Docker is an open-source platform used to develop, package, distribute, and run applications inside isolated environments called **containers**.

A container includes everything an application needs to run, such as:

* Application code
* Libraries
* Dependencies
* Configuration files

Docker helps ensure that applications run consistently across different environments, whether on a developer's machine, a testing environment, or a production server.

Unlike traditional virtual machines, Docker containers share the host operating system kernel, making them lightweight and efficient.

---

## Key Concepts

### Image

A **Docker Image** is a read-only template used to create containers.

It contains:

* Application code
* Dependencies
* Libraries
* Configuration files

An image itself is not running. It serves as a blueprint from which containers are created.

### Container

A **Docker Container** is a running instance of a Docker image.

Containers provide isolated environments where applications can run independently from the host system and other containers.

Characteristics of containers:

* Lightweight
* Portable
* Isolated
* Easy to deploy

### Port Mapping

**Port Mapping** is the process of connecting a port on the host machine to a port inside a container.

This allows services running inside a container to be accessed from outside the container.

**Example:**

```text
3000:3000
```

```text
Host Port : Container Port
```

In this example:

* The application runs on port `3000` inside the container.
* The host machine exposes the application through port `3000`.

This allows applications running inside a container to be accessed through a web browser or other tools on the host machine.

### Volume

A **Docker Volume** is a storage mechanism used to persist data outside a container.

Containers do not permanently store data by default. If a container is deleted, its data may be lost.

Docker volumes provide persistent storage that remains available even if a container is stopped, deleted, or recreated.

Common use cases:

* Databases
* Logs
* Application data
* Configuration files

### Docker Daemon

The **Docker Daemon** (`dockerd`) is a background service that manages Docker resources and handles Docker operations.

Responsibilities include:

* Downloading images
* Creating containers
* Starting containers
* Stopping containers
* Managing networks
* Managing volumes

Docker commands communicate with the Docker Daemon to perform these actions.

---

## Why Docker is Useful

Docker provides several benefits:

* Consistent application deployment across environments
* Lightweight compared to virtual machines
* Faster startup times
* Easy application distribution
* Isolation between applications
* Simplified testing and development environments

In cybersecurity, Docker is commonly used to create isolated lab environments for practicing security testing and running vulnerable applications safely.

---

## What I Learned

* Docker is a platform for running applications inside containers.
* Images are templates used to create containers.
* Containers are running instances of images.
* Containers are lighter than virtual machines because they share the host operating system kernel.
* Port mapping exposes container services to the host machine.
* Docker volumes provide persistent storage for containers.
* The Docker Daemon manages Docker resources in the background.
* Docker is useful for creating isolated cybersecurity lab environments.

