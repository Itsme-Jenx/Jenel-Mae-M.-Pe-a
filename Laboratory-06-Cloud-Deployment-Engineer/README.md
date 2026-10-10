# Mission 6: Cloud Deployment Engineer

**Course:** CCM 101 - Cloud Computing  
**Student:** Jenel Mae M. Peña
**Section:** BSIT 4-F  
**Institution:** University of Eastern Pangasinan

## Mission Overview

This mission focuses on deploying a private cloud storage platform using Docker Compose. The project combines Nextcloud, which provides the web interface, and MariaDB, which manages the application's database. Both services are described in a single configuration file to make deployment more convenient.

## Objectives

- Describe the functions of a two-tier application.
- Understand how Docker Compose manages multiple services.
- Create a Docker Compose configuration using the nano editor.
- Run Nextcloud and MariaDB as separate containers.
- Access the Nextcloud installation page through a browser.
- Apply Infrastructure as Code concepts in a practical activity.

## Commands Executed

The following commands were used during the laboratory activity:

```bash
docker --version
docker-compose --version
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
docker-compose config
docker-compose up -d
docker-compose ps
docker-compose logs
docker-compose down
```

## Skills Learned

- Creating and validating YAML configuration files.
- Managing multiple Docker services.
- Connecting an application to a database.
- Publishing a containerized web application through port mapping.
- Monitoring container status and checking logs.
- Writing technical documentation in Markdown.

## Deployment Evidence

The `screenshots/` directory contains the following evidence:

1. `compose-deployment.png` — Shows the deployment and container status.
<img width="1242" height="591" alt="image" src="https://github.com/user-attachments/assets/1f66506a-667f-41aa-a14f-5389a0c30f20" />

2. `nextcloud-web.png` — Shows the Nextcloud installation interface.
<img width="1917" height="867" alt="image" src="https://github.com/user-attachments/assets/f649d850-f4dc-4c36-b89b-9b2bb39a1af1" />

3. `compose-teardown.png` — Shows the removal of the deployed containers.
<img width="1157" height="141" alt="image" src="https://github.com/user-attachments/assets/4c417d98-2039-4cb8-bdd8-2757ea669028" />


## Documentation

- [Two-Tier Architecture](multi-tier-architecture.md)
- [Docker Compose Documentation](docker-compose-guide.md)
- [Personal Reflection](reflection.md)
