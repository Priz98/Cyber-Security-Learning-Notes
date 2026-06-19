# Docker

## Whats is Docker?

Docker is a platform used to run applications in isolated environments called containers.
Containers package an application with everything it needs to run, making deployment consistent across different systems.

It does this by using these features: 

## Features

1.  Image : A Docker image is a template used to create containers. It consists of Application code, Dependencies, Configuration files.
2.  Container : A container is a running instance of a Docker image. Containers provide isolated environments for applications.
3.  Volume : Containers do not permanently store data by default. If a container is removed, any data stored inside it may also be lost.
Docker Volumes provide persistent storage that exists independently of containers. This allows data to remain available even if a container is stopped, deleted, or recreated.

## Why Docker is Included in This Repository: 

Docker is used to create isolated lab environments for cybersecurity practice.

It allows vulnerable applications and security tools to run safely without affecting the host system.

## What I Learned:

1. Images are used to create containers.
2. Containers are running instances of images.
3. Port mapping exposes container services to the host.
4. Docker provides isolated environments for labs and testing.
