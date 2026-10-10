# Understanding Two-Tier Application Architecture

## Definition

A two-tier architecture is a system in which an application and its database operate as two separate components. Each component has a specific responsibility, and they communicate to complete the application's operations.

For this deployment, the two components are the Nextcloud web application and the MariaDB database.

## Web/Application Tier

The web or application tier is responsible for interacting with users. It presents the website, receives browser requests, and processes the actions performed by users.

Nextcloud serves as this tier in our project. It provides the interface for a private cloud storage service and communicates with the database whenever it needs information about users, files, or application settings.

## Database Tier

The database tier handles the storage and organization of application data. It allows the application to save, retrieve, and update information when necessary.

MariaDB performs this role in our deployment. It stores the database information required by Nextcloud, including account-related information and file metadata. The database service is configured separately from the web application.

## Advantages of Separating the Tiers

Keeping the application and database in separate containers makes maintenance more manageable because each component can be updated or troubleshot independently. It also makes it easier to allocate resources and expand individual services when necessary. Separating containers alone does not guarantee security, so access permissions, network restrictions, and proper credential handling are still important.

## How the Components Communicate

The browser connects to Nextcloud through the published host port 8080, which forwards requests to port 80 inside the application container. Nextcloud then connects to MariaDB using the hostname `database`, which corresponds to the database service defined in Docker Compose.

**Architecture flow:**

User's Browser → Nextcloud Web Application → MariaDB Database

This design separates the user-facing application from the service responsible for storing its data.
