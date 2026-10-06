# Docker Compose Guide

## The Compose File
```yaml
version: '3'

services:
  database:
    image: mariadb:10.6
    environment:
      - MYSQL_ROOT_PASSWORD=cloudnova_root
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user

  app:
    image: nextcloud
    ports:
      - 8080:80
    environment:
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user
      - MYSQL_HOST=database
```

## What does the `services:` block do?
The `services:` block is where the containers of the application are listed.
Each name under it is one container. In this file there are two, `database`
(MariaDB) and `app` (Nextcloud). Under each one, the image, ports, and
environment variables are set, so Docker knows what to run and how to
configure it.

## How did the Nextcloud container find the database?
Through the `MYSQL_HOST=database` line. The word `database` is the same as
the service name in the file. Docker Compose puts both containers on the same
network, and on that network the service name works like a hostname. So
Nextcloud just connects to `database` and Docker takes it to the MariaDB
container, with no IP address needed.

## What is the difference between `docker run` and `docker-compose up -d`?
`docker run` starts only one container, and everything like the image, ports,
and settings has to be typed in the command each time. For two containers
that needs two long commands, plus extra work to connect them.

`docker-compose up -d` reads the `docker-compose.yml` file and starts
everything at once, including the network between the containers. The `-d`
makes it run in the background so the terminal stays free to use. It's also
easy to repeat, since the whole setup is saved in the file.
