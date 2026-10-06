# Reflection

It is important to check the host server's resources even if the containers
are running perfectly because all containers share the resources of the host.
If the host runs out of memory, disk space, or CPU, every container on it can
slow down or crash, even if each one looks healthy on its own.

If a user complains that they cannot log into a web application, the docker
logs command can help me find the problem. The logs show the requests that
reached the container and the errors that happened, so I can see exactly what
failed and when. In this lab, the 404 line in the logs showed me how a single
failed request can be traced.

Monitoring logs and monitoring metrics are different. Logs are a record of
events, like each request, its time, and its result, so they tell what
happened. Metrics are numbers like CPU, memory, and network usage, so they
tell how the container is performing in real time. Logs help find the cause
of a problem, while metrics help show if the system is healthy or getting
overloaded.

Large enterprise companies probably monitor thousands of containers using
tools like Prometheus and Grafana. Prometheus collects metrics from all the
containers automatically, and Grafana shows them in dashboards. They can also
send alerts when something goes wrong, so engineers do not have to check each
container one by one.

My ability to troubleshoot Linux environments has improved a lot in this lab.
Before, I did not know how to check the health of a server. Now I can use
commands like free -h, df -h, and top to check the host, and docker logs and
docker stats to check a container. I feel more confident that I can find out
what is wrong instead of just guessing.
