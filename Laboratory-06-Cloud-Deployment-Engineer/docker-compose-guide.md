# Guide to Deploying Applications with Docker Compose

## Overview

Docker Compose simplifies the management of applications that need multiple containers. Instead of configuring every container through separate commands, an engineer can describe the required services in a YAML file and manage them together.

In this mission, the configuration contains Nextcloud and MariaDB.

## Understanding the Services Section

The `services:` section lists the components that Docker Compose must manage.

The configuration contains two services:

- **database:** Runs MariaDB version 10.6 and provides database functionality.
- **app:** Runs Nextcloud and makes its web interface accessible through port 8080.

Each service specifies the container image and the settings needed to run it.

## Environment Variables

Environment variables provide configuration values to the containers.

The database service uses the following variables:

- `MYSQL_ROOT_PASSWORD` — Defines the MariaDB root password.
- `MYSQL_DATABASE` — Identifies the database used by the application.
- `MYSQL_USER` — Defines the application's database account.
- `MYSQL_PASSWORD` — Specifies the password for that account.

The Nextcloud service uses the database name, username, and password to connect to MariaDB.

These credentials are suitable only for the classroom demonstration. In a real deployment, passwords should be managed through a more secure mechanism rather than stored directly in a shared configuration file.

## Database Service Discovery

The Compose file contains this setting:

```yaml
- MYSQL_HOST=database
```

The hostname `database` matches the name assigned to the MariaDB service. Docker Compose provides internal service discovery, so Nextcloud can use this hostname to reach the database without requiring the database container's IP address to be entered manually.

Both services must be configured correctly and the database must be ready to accept connections.

## Understanding Port Mapping

The following configuration exposes the Nextcloud web interface:

```yaml
ports:
  - 8080:80
```

The first port, `8080`, is the host-side port. The second port, `80`, is the port inside the Nextcloud container. This mapping allows users to access the web application through the environment's exposed port.

## Comparing Docker Run and Docker Compose

### Docker Run

`docker run` starts an individual container with the options supplied in a command. For an application with several dependent services, separate commands and additional configuration may be needed.

### Docker Compose

`docker-compose up -d` reads the Compose file and starts the defined services in the background. It keeps the deployment settings in one place, making the application easier to recreate and maintain.

The command `docker-compose down` stops and removes the Compose-managed containers and network. Persistent named volumes are retained unless volume removal is explicitly requested.

## Deployment Commands

```bash
docker-compose config
docker-compose up -d
docker-compose ps
docker-compose logs
docker-compose down
```

On systems with the Compose v2 plugin, the equivalent commands use `docker compose` with a space instead of `docker-compose`.

## Conclusion

Docker Compose makes multi-container deployment more organized by keeping service definitions and configuration in one file. This mission demonstrates how a web application and its database can work together as a single manageable application stack.
