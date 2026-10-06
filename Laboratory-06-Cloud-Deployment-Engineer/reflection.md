# Reflection

Writing a docker-compose.yml file makes a cloud engineer's job a lot easier
because everything is written in one place. Without it, I would have to type
a long command for each container and connect them by myself, and one small
typo could break the setup. With Compose, one command starts the whole stack,
and the file can be reused or shared with other engineers anytime.

If there is an indentation error in a YAML file, like using a Tab instead of
Spaces, Docker Compose will not be able to read the file properly. YAML
depends on spaces to know which settings belong to which service, so a wrong
indentation gives an error or puts the settings in the wrong place. That is
why I had to be careful when typing the file in nano.

Environment variables like MYSQL_PASSWORD were used so the containers can be
configured without changing the images. The database uses them to create the
user, password, and database, and Nextcloud uses the same values to connect
to it. It also keeps the settings in one place, so they are easy to change
later.

Deploying a working enterprise cloud storage system in just a few minutes
felt amazing. I expected a long installation and a lot of setup, but after
one command, Nextcloud was already running in the browser. I also made a
mistake when I ran docker-compose down in the wrong folder, but I learned
that the command has to be run where the Compose file is.

Since Mission 1, my understanding of cloud computing has changed a lot.
Before, I only thought of it as using services over the internet. Now I know
how to deploy containers, connect them, and manage them using code. I see
now that the cloud is something you can build and control yourself, not just
use.
