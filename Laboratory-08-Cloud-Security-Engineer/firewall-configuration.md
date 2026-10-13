# Firewall Configuration

This document lists the commands used to secure the Ubuntu server with UFW (Uncomplicated Firewall).

## 1. Allow SSH
```bash
sudo ufw allow ssh
```
Allows port 22 so administrators can still manage the server remotely.

## 2. Set the Default Deny Policy
```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```
Blocks all incoming traffic by default, while still allowing the server to make outgoing connections.

## 3. Allow Port 8080
```bash
sudo ufw allow 8080/tcp
```
Opens TCP port 8080 so users can reach the Nginx web application (`secure-web-app`).

## What happens if `ufw enable` runs before `ufw allow ssh`?
The firewall would start with a default deny policy and no rule for port 22, so the SSH connection would be blocked and the administrator would be locked out of the server.
