### Setup cron jobs

- crontab -e

Script to run

#!/bin/bash

### Define the log file location
LOG_FILE="/home/user/cron_log.txt"

### Write the current date and time to the log file
echo "Script executed at: $(date)" >> "$LOG_FILE"

### Make script executable

- chmod +x log_date.sh

### Run on Mondays at 1pm

- 0 13 * * 1 /home/user/log_date.sh

### Script output

- tail -f cron_log.txt

Script executed at: Mon Nov 25 06:13:01 PM PST 2024
Script executed at: Mon Nov 25 06:14:01 PM PST 2024

### Schedule tasks with at

- echo "command" | at now + 5 minutes
