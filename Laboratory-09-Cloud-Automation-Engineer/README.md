## Mission Overview
Traditionally, systems administrators manage servers by typing commands manually, one by one. In large enterprise environments that scale to thousands of servers, this approach is too slow and highly prone to human error. To work at that scale, automation is essential.

Using the KillerCoda Playground, this mission put the role of a Cloud Automation Engineer into practice. It covered the basics of Bash shell scripting, the creation of an automated backup routine, the assignment of executable permissions to the script, and the configuration of the Linux Cron scheduler so the script runs on its own. The guiding principle is simple: any task that has to be done more than twice in the cloud should be automated.

## Objectives
- Understand the fundamental syntax of a Bash shell script, including variables and basic commands.
- Use a command-line text editor (nano) to write and save executable scripts.
- Modify Linux file permissions using the chmod command.
- Understand task scheduling and the syntax of a crontab.
- Document automation code and Cron job configurations using Markdown.
- Complete the final chapter of your GitHub Cloud Computing Portfolio.

## Commands Executed
```bash
mkdir app-data
echo "This is critical client data." > app-data/data.txt
nano backup.sh
./backup.sh
chmod +x backup.sh
./backup.sh
ls -l backups/
crontab -l
env EDITOR=nano crontab -e
crontab -l
```

## Skills Learned
- Writing a Bash script with variables
- Compressing data into a .tar.gz backup with `tar`
- Changing file permissions with `chmod +x`
- Scheduling recurring tasks with cron
- Documenting automation work in Markdown
