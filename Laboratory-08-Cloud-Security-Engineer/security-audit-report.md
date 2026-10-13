# Security Audit Report

## The Principle of Least Privilege (PoLP)
The Principle of Least Privilege means a user, program, or process should only get the minimum permissions it needs to do its job. It matters for cloud accounts because it limits the "blast radius" of a breach. For example, if an intern only needs to read sales reports, giving them read-only access means a stolen laptop can't be used to delete the whole database.

## Attack Surface
For a virtual machine, the attack surface is every service, application, and open port that an attacker could try to use to get in. Each piece of running software is a possible door, so the more unnecessary services a server runs, the bigger its attack surface. Disabling or removing anything the server doesn't need shrinks it and removes vulnerabilities an attacker could exploit.

## Default Deny Policy
A default deny policy means the firewall blocks all incoming traffic unless a rule specifically allows it. This is safer than blocking individual hackers because you can't predict every malicious IP or new attack, but you do know the few services your server actually needs, like SSH and the web app. Locking everything down first and then opening only those ports leaves attackers with far fewer ways in.
