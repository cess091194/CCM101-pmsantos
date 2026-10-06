## Mission Overview
CloudNova Technologies has a client, a university, that wants to stop paying
for Google Drive and host its own private, secure cloud storage system. This
mission was to deploy a proof-of-concept Nextcloud environment using a
two-tier architecture: a MariaDB database container and a Nextcloud web
container, linked together using Docker Compose in a KillerCoda Ubuntu
Playground.

## Objectives
- Explain the concept of a multi-tier application architecture
- Understand the purpose and structure of a `docker-compose.yml` file
- Use a Linux command-line text editor (nano) to create configuration files
- Deploy a multi-container application (Nextcloud + Database) using Docker Compose
- Document deployment procedures and Infrastructure as Code (IaC) principles using Markdown
- Continue expanding a professional GitHub Cloud Computing Portfolio

## Commands Executed
```bash
mkdir nextcloud-deployment      # create the project directory
cd nextcloud-deployment         # move inside the directory
nano docker-compose.yml         # create and edit the Compose file
docker-compose up -d            # deploy both containers in the background
docker-compose ps               # check that the containers are running
docker-compose down             # stop and remove the containers
```

## Skills Learned
- Explaining and building a two-tier (multi-tier) architecture
- Writing a YAML file with correct indentation
- Defining multiple services in one Docker Compose file
- Using environment variables to configure containers
- Deploying and tearing down a multi-container stack with a few commands
- Understanding how containers find each other using service names
- Applying Infrastructure as Code (IaC) principles by defining the whole deployment in a single YAML file
- Documenting deployment procedures in Markdown
- Using the nano text editor to create configuration files in the Linux terminal
