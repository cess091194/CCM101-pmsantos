# Reflection

A host-based firewall protects a server even when the physical network perimeter has been breached because it sits on the server itself. If an attacker gets past the outer defenses, the firewall still inspects every incoming packet and drops anything that was not explicitly allowed. With a Default Deny policy, one failed layer does not expose everything, which is the core idea behind defense in depth.

This is closely tied to managing open ports. Every open port is a door into the server, because a service is listening behind it, and the more doors there are, the more chances an attacker has to find a weakness. In this lab, only SSH and port 8080 were allowed, so everything else stayed closed. A small attack surface is harder to exploit and easier to monitor.

The same reasoning explains why leaving a database port like 3306 for MySQL open to the public internet is dangerous in a real enterprise. Anyone in the world could try to connect, and automated bots constantly scan for exposed databases to attempt brute-force logins or known exploits. If one succeeds, attackers could steal or delete sensitive data, causing breaches, legal trouble, and lost customer trust. A database should only be reachable by the application servers that need it.

Completing this mission changed how I see server security. Before the lab, I assumed a server was reasonably safe as long as it was running normally. Now I understand that one forgotten setting, like a missing firewall, can leave it exposed within minutes. The warning about allowing SSH first also showed that even the order of commands matters, since enabling UFW too early could lock an administrator out.

With eight completed missions, the GitHub portfolio now shows a clear progression from basic cloud concepts to deployment, operations, and security. Each laboratory has its own folder with documentation and screenshots, so the repository reads like a real record of hands-on work.
