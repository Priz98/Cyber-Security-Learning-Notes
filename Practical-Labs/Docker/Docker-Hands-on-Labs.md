# Docker Hands on Labs

## Firstly I installed Docker itself by visiting Docker's Website.

[Docker Desktop Windows Installation Guide](https://docs.docker.com/desktop/setup/install/windows-install/)

After Setting up Docker Desktop. 
Access CLI and performed Commands like.

### 1. Pull Image and Run Container

This commands are used to get docker image from Docker hub. 

```bash
docker pull ubuntu
```

This Command is used to Create and Run a Docker Container using the downloaded Image.

```bash
docker run -it ubuntu
```

![Alt text for screen readers](Images/Image-Pull-n-Create-Container.png)
![Alt text for screen readers](Images/Created-Container.png)

### 2. Listing Container

This commands is used to list all containers made in Docker. 

```bash
docker ps -a
```

![Alt text for screen readers](Images/Container-list.png)
