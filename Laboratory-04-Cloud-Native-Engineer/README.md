## Mission Overview
In this lab, I took on the role of a Cloud-Native Engineer at CloudNova Technologies. The client I was working with was still using traditional Virtual Machines and wanted to understand why containers might be a better option. My task was to research the differences between VMs and containers, then use Docker to deploy, manage, and remove a containerized Nginx web server as a live demonstration.

## Objectives
- Differentiate between VMs and Containers
- Access a Docker-enabled environment using KillerCoda
- Execute fundamental Docker CLI commands
- Deploy and manage a containerized Nginx application
- Document container operations professionally

## Docker Commands Executed
- `docker --version`
- `docker info`
- `docker pull nginx`
- `docker run -d -p 8080:80 --name my-nginx nginx`
- `curl http://localhost:8080`
- `docker ps`
- `docker stop my-nginx`
- `docker ps -a`
- `docker rm my-nginx`

## Skills Learned
Through this lab, I learned how to pull an image from Docker Hub, run a container in detached mode, and map a host port to a container port so I could access the web server. I also learned the basic container lifecycle commands for checking, stopping, verifying, and removing a container.

## Challenges Encountered
Overall, this lab went smoothly for me. The only part I had to slow down on was making sure I understood the port mapping syntax (`-p 8080:80`), since I wanted to be clear on which number was the host port and which was the container port before running the command.
