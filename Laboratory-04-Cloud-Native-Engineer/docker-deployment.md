# Docker Deployment & Container Lifecycle Documentation

## Docker Commands Executed and Descriptions

### Docker Environment Verification

1. `docker --version`
   - **Explanation:** Displays the installed Docker version and confirms that Docker is available in the KillerCoda environment.

2. `docker info`
   - **Explanation:** Displays detailed information about the Docker environment and verifies that the Docker engine is running properly.

### Nginx Container Deployment

3. `docker pull nginx`
   - **Explanation:** Downloads the official Nginx image from Docker Hub so it can be used to create an Nginx container.

4. `docker run -d -p 8080:80 --name nginx-server nginx`
   - **Explanation:** Creates and runs the Nginx container in detached mode, mapping port `8080` on the host to port `80` inside the container.

5. `docker ps`
   - **Explanation:** Displays the active Nginx container and shows information such as the container ID, image, status, ports, and container name.

6. `curl http://localhost:8080`
   - **Explanation:** Sends an HTTP request to the Nginx web server through port `8080` and verifies that the containerized web server is working correctly.

## Container Lifecycle Commands

7. `docker ps`
   - **Explanation:** Displays all active, currently running containers.

8. `docker stop nginx-server`
   - **Explanation:** Stops the running `nginx-server` container gracefully without removing the container.

9. `docker ps -a`
   - **Explanation:** Lists all containers on the host system, including running and stopped containers, allowing the stopped Nginx container to be verified.

10. `docker rm nginx-server`
    - **Explanation:** Permanently removes the stopped `nginx-server` container from the Docker environment.

11. `docker ps -a`
    - **Explanation:** Verifies that the `nginx-server` container has been removed and no longer appears in the container list.

## Terminal Output Screenshot

The screenshots below show the execution and results of the Docker commands used during the laboratory activity.



### Container Lifecycle

![Container Lifecycle](screenshots/container-lifecycle.png)
<img width="1527" height="290" alt="image" src="https://github.com/user-attachments/assets/c9fca4ff-1517-426c-bfe6-7a5d2751b059" />
