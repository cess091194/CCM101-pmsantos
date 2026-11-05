# Final Reflection

When I started Mission 1, I didn't know much about the Linux terminal. Git and GitHub confused me, and I was just following the steps one by one. After ten missions, I can set up and manage a server on my own, and cloud computing makes a lot more sense to me now.

In Mission 2, I learned how to check a server's CPU, storage, and network. `lscpu` didn't work, so I used `cat /proc/cpuinfo` instead. In Mission 3, I learned that AWS, Azure, and GCP have almost the same services, and that the best one depends on what the client needs.

Mission 4 was about Docker, and I was surprised that a container starts in seconds while a VM takes minutes. In Mission 5, the MinIO image from the handout gave me a "pull access denied" error, so I had to find another image that worked. In Mission 6, Docker Compose saved me from typing long commands, but I ran `docker-compose down` in the wrong folder once and learned to check where I am first. Mission 7 taught me to check if a server is healthy using logs, `docker stats`, `free -h`, and `df -h`. In Mission 8, I set up a firewall and learned that allowing SSH first is important. In Mission 9, I used Bash scripts and scheduled jobs to automate tasks.

Mission 10 put everything together. We built an Ubuntu Server VM in VirtualBox, deployed WordPress and MariaDB with Docker Compose, set up a Default Deny firewall, and scheduled a nightly database backup. The hardest part was making all of it work together. When something broke, I read the error, checked the logs, and looked for another way instead of guessing.

The biggest thing I learned is that small details matter. A wrong space in a YAML file, the order of firewall commands, or the wrong folder can break the whole setup. I also learned that writing good documentation is part of the work, so that someone else can understand and repeat what I did.

My GitHub portfolio now shows my progress, from simple Linux notes in Mission 1 to a full server project in Mission 10. I feel more confident that I can build, secure, and take care of a small cloud setup.
