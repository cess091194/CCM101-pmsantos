## Mission Overview
In earlier missions, only single containers were deployed, like a standalone
web server or a storage bucket. Real-world enterprise applications are
usually multi-tier systems, where a frontend web application communicates
with a backend database. Deploying each container manually one by one can
easily lead to mistakes.

This mission introduces Docker Compose and the shift from manual commands to
Infrastructure as Code (IaC). A YAML file was used to define a multi-container
private cloud storage application (Nextcloud and MariaDB), and the whole
stack was deployed with a single command in a KillerCoda Ubuntu Playground.

A junior engineer deploys servers by typing commands; a senior engineer
deploys infrastructure by writing code.

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
