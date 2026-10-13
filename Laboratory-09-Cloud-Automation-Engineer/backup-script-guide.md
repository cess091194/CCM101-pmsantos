# Backup Script Guide

This guide documents the automated backup script created for CloudNova Technologies so the client's IT team can understand how it works.

## The Script (`backup.sh`)
```bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p $BACKUP_DIR

# Compress the source directory into a tarball (.tar.gz)
tar -czf $BACKUP_DIR/backup_$TIMESTAMP.tar.gz $SOURCE_DIR

echo "Backup completed successfully at $TIMESTAMP!"
```

## What `chmod +x` Does
The `chmod +x backup.sh` command adds the execute permission to the file. By default, Linux treats a new file as plain text, so without this permission the script cannot be run as a program and returns "Permission denied".

## Cron Expression
```
0 2 * * * /root/backup.sh
```

| Field | Value | Meaning |
|---|---|---|
| Minute | 0 | At minute 0 |
| Hour | 2 | At 2 AM |
| Day of Month | * | Every day of the month |
| Month | * | Every month |
| Day of Week | * | Every day of the week |

Together, the script runs every night at exactly 2:00 AM.
