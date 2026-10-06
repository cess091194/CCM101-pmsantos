# Two-Tier Architecture

## Overview
A two-tier architecture is a way of building an application by splitting it
into two separate layers: one that users interact with, and one that stores
the data. The two layers run on their own and talk to each other over a
network. In this lab, the two tiers are the Nextcloud container (the
application tier) and the MariaDB container (the database tier), which are
linked together using Docker Compose.

## The Web/Application Tier
The web/application tier is the part of the system that users actually see
and use. Its main jobs are:

- Serving the user interface, which is the Nextcloud web pages in the browser
- Handling HTTP requests coming from users
- Running the application logic, like logging in, uploading files, and
  sharing folders
- Sending queries to the database whenever it needs to get or save data

In this laboratory activity, this is the `app` service running the `nextcloud` image. It is
exposed on port 8080 so it can be accessed through the browser.

## The Database Tier
The database tier is where all the important data is stored. Its main jobs are:

- Storing persistent data such as user accounts and credentials
- Keeping file metadata, like file names, owners, and permissions
- Keeping the data organized and safe, even if the app container restarts
- Only answering requests from the application tier, so users never talk to
  it directly

In this laboratory activity, this is the `database` service running `mariadb:10.6`.

## Why Separate Them?
Putting the web server and the database in two separate containers makes the
system easier to manage, because either one can be updated, restarted, or
fixed without breaking the other. It is also more secure since the database is
hidden behind the application and isn't directly exposed to users. If the
system grows later, each tier can be scaled on its own instead of having to
scale everything together.
