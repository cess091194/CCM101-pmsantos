# Reflection

Automation is critical when managing hundreds of cloud servers because doing the same task by hand on every machine is slow and full of chances for mistakes. A script can run the same steps on one server or a thousand and get the same result every time. A scheduled job like cron also makes sure routine work, such as backups, happens on time without anyone having to remember it.

Still, automation has its dangers. A script does exactly what it is told, so a destructive typo, like deleting the wrong folder, would not affect just one server but every server the script is scheduled to run on. Data could be wiped out within minutes, before anyone notices. This is why scripts should be tested on a small setup first and reviewed carefully before they are scheduled widely.

Writing a Bash script also felt different from creating the Docker Compose YAML file in Mission 6. A Compose file is declarative, meaning it describes what the setup should look like, such as which containers and ports to use, and Docker figures out how to build it. A Bash script is step by step, so the order of the commands, the variables, and the file permissions all matter. The script would not even run until it was given execute permission with chmod.

Looking back at the repository from Laboratory 1 to Laboratory 9, the understanding of cloud computing has changed a lot. At the start, the cloud was only a vague idea of servers somewhere online. Now it is clear that it is a set of skills that build on each other: deploying applications, using containers, operating servers, securing them, and finally automating the work.

The role that stood out the most was the Security Engineer. Locking down a live server with UFW showed the effect of every command right away, and the warning about allowing SSH first made the work feel like a real job where one wrong step has consequences.
