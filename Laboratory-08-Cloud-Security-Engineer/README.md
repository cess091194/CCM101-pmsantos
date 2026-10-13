## Mission Overview
This laboratory activity places the learner on the Cloud Security Team at CloudNova Technologies, applying the security concepts from Chapter 8. A server left unsecured, even for a few minutes, can be hit by automated brute-force attacks and data breaches. To prevent this, the activity follows the principle of defense in depth by locking down a live Ubuntu server with a host-based firewall. Using the KillerCoda Playground, a web application was deployed, the server's open ports were audited, and the Uncomplicated Firewall (UFW) was configured to block malicious traffic while still letting legitimate users reach the application. The key takeaway is that security is not a product to buy but a continuous process to maintain.

## Objectives
- Understand the concept of the Attack Surface and the Principle of Least Privilege (PoLP).
- Perform a basic security audit of active network ports on a Linux server.
- Configure the Uncomplicated Firewall (UFW) with a Default Deny policy.
- Implement granular port management to selectively allow SSH and HTTP traffic.
- Document firewall rules and security best practices using Markdown.
- Continue expanding your professional GitHub Cloud Computing Portfolio.

## Commands Executed
```bash
# Deploy the web application
docker run -d --name secure-web-app -p 8080:80 nginx
docker ps
curl http://localhost:8080

# Build the firewall
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw status verbose

# Granular port management
sudo ufw allow 8080/tcp
sudo ufw status numbered
curl http://localhost:8080
```

## Skills Learned
- Deploying a containerized web server with Docker
- Auditing which ports are exposed on a server
- Configuring UFW with a Default Deny incoming policy
- Allowing specific services (SSH and port 8080) with granular rules
- Verifying firewall rules with `ufw status` and testing access with `curl`
- Documenting technical work in Markdown
