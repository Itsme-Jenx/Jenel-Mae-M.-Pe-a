# Mission 4 Reflection

This laboratory activity helped me understand the difference between Virtual Machines (VMs) and Docker containers and how containerization can make application deployment easier. In a Virtual Machine, a complete operating system needs to be installed and started before applications can run. This usually takes more time and requires more RAM and storage. In comparison, a Docker container uses the host operating system and only contains the application and its required files. Because of this, containers can start much faster and use fewer resources. In this activity, I was able to deploy an Nginx web server using only a few Docker commands.

The port mapping `-p 8080:80` is necessary because the Nginx web server is running inside the container. Port `80` is the port used by Nginx inside the container, while `8080` is the port exposed on the host. This mapping allows the host system to communicate with the Nginx server inside the container. I was able to test this connection by using `curl http://localhost:8080` and seeing the Nginx welcome page.

When the `docker rm` command is used, the specified stopped container is permanently removed. Any data stored only inside the container may also be lost when the container is removed. This shows why important application data should be stored using persistent storage such as Docker volumes when necessary.

Containerization also changes how software developers and IT operations teams work together. Developers can package applications with their required dependencies in containers, while IT operations teams can deploy the same containers in different environments. This supports DevOps by making development, testing, and deployment more consistent.

My GitHub portfolio is also evolving as I complete more cloud computing activities. Laboratory 4 adds practical Docker experience, technical documentation, screenshots, and reflection to my previous work. It shows my progress in learning cloud technologies and gives me a more organized record of the skills and activities I have completed.
