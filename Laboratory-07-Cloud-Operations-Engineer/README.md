## Mission Overview
After deploying multi-tier architectures, this mission moves into the Cloud
Operations (Site Reliability Engineering) side of CloudNova Technologies.
Deploying a cloud application is only the first step, because keeping it
running smoothly is the real challenge. When a server crashes or a web page
loads slowly, guessing is not enough, so Observability and Monitoring are
needed to see inside the infrastructure.

Using a KillerCoda Ubuntu Playground, a performance baseline of the Linux
server was established, an Nginx web container was deployed, artificial web
traffic was generated, and the application logs and container metrics were
collected to prove that the application was healthy.

A developer hopes the application works; a Site Reliability Engineer uses
metrics and logs to prove it.

## Objectives
- Utilize native Linux command-line tools to monitor host CPU, Memory, and Disk capacity
- Deploy a web container and track its real-time performance using Docker metrics
- Generate web traffic and extract application access logs for analysis
- Translate raw performance data into a readable technical report using Markdown
- Continue expanding a professional GitHub Cloud Computing Portfolio

## Monitoring Commands Executed
```bash
free -h                                              # check host memory (RAM) usage
df -h                                                # check host disk storage
top                                                  # view running processes and CPU load
docker run -d -p 8080:80 --name client-website nginx # deploy the Nginx web container
curl http://localhost:8080                           # simulate users visiting the website
curl http://localhost:8080/hidden-admin-page         # generate a 404 error
docker logs client-website                           # view the application logs
docker stats                                         # view real-time container metrics
```

## Skills Learned
- Checking host CPU, memory, and disk capacity using Linux commands
- Establishing a system performance baseline
- Deploying a containerized web server with Docker
- Generating test traffic using `curl`
- Reading application logs to find successful requests (200) and errors (404)
- Monitoring real-time container CPU, memory, and network usage with `docker stats`
- Understanding the difference between logs and metrics in observability
- Documenting monitoring results in Markdown
