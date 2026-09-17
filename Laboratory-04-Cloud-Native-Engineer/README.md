# Laboratory Activity 04: The Cloud-Native Engineer

## Mission Overview

This laboratory activity introduces the basic concepts of cloud-native engineering and containerization using Docker. The activity focuses on understanding the differences between traditional Virtual Machines (VMs) and Containers and learning how containers can be used to deploy applications quickly and efficiently.

In this activity, I researched the differences between Virtual Machines and Containers, accessed a Docker-enabled environment using KillerCoda, verified the Docker installation, deployed an Nginx web server using Docker, tested the web server using a local HTTP request, and practiced basic container lifecycle management.

## Objectives

- Differentiate the architecture, boot time, resource efficiency, and isolation level of Virtual Machines and Containers.
- Access and use a Docker-enabled cloud environment through KillerCoda.
- Execute fundamental Docker CLI commands.
- Pull and run an Nginx containerized web server.
- Use port mapping to make the Nginx web server accessible.
- Test the containerized web server using `curl`.
- Stop, verify, and remove a Docker container.
- Create technical documentation using Markdown.
- Continue developing an organized GitHub Cloud Computing Portfolio.

---

## Technical Reports & Documents

- **Virtual Machines vs. Containers:** [virtualization-vs-containers.md](virtualization-vs-containers.md)
- **Docker Deployment & Lifecycle:** [docker-deployment.md](docker-deployment.md)
- **Mission Reflection:** [reflection.md](reflection.md)

---

## Docker Commands Executed

### 1. Docker Environment Verification

- `docker --version` — Displays the installed Docker version and confirms that Docker is available in the KillerCoda environment.
- `docker info` — Displays detailed information about the Docker environment and verifies that the Docker engine is running properly.

### 2. Nginx Container Deployment

- `docker pull nginx` — Downloads the official Nginx image from Docker Hub.
- `docker run -d -p 8080:80 --name nginx-server nginx` — Creates and runs the Nginx container in detached mode and maps host port `8080` to container port `80`.
- `docker ps` — Displays the currently running Nginx container and its basic information.
- `curl http://localhost:8080` — Sends an HTTP request to the Nginx web server and verifies that it is running successfully.

### 3. Container Lifecycle Operations

- `docker ps` — Lists the currently running containers.
- `docker stop nginx-server` — Stops the running Nginx container.
- `docker ps -a` — Lists all containers, including running and stopped containers.
- `docker rm nginx-server` — Permanently removes the stopped Nginx container.
- `docker ps -a` — Verifies that the removed Nginx container no longer appears in the container list.

---

## Evidence Screenshots

The command output screenshots are stored inside the `screenshots/` directory:

- **Docker Environment Verification:** `screenshots/docker-version.png`
- **Nginx Container Deployment:** `screenshots/nginx-running.png`
- **Container Lifecycle:** `screenshots/container-lifecycle.png`

---

## Skills Learned

- Basic Docker Command Line Interface operations.
- Understanding the differences between Virtual Machines and Containers.
- Understanding container images and containers.
- Pulling Docker images from Docker Hub.
- Deploying an Nginx web server using Docker.
- Using host-to-container port mapping.
- Testing a web server using the `curl` command.
- Managing the Docker container lifecycle.
- Using Linux terminal commands.
- Writing technical documentation using Markdown.
- Organizing and maintaining a GitHub Cloud Computing Portfolio.

## Challenges Encountered

One challenge I encountered was understanding the difference between Virtual Machines, Docker images, and containers. I learned that a Virtual Machine runs a complete operating system, while a Docker image is a template used to create a container. Another challenge was understanding the port mapping `8080:80`. After testing the Nginx server using `curl`, I understood that port `8080` on the host connects to port `80` inside the container.

I also needed to become familiar with Docker commands such as `docker pull`, `docker run`, `docker ps`, `docker stop`, and `docker rm`. By following the commands step by step in the KillerCoda environment, I was able to understand the basic Docker container lifecycle and successfully deploy and manage an Nginx web server.
