### Locate and interpret system log files
- journalctl

### Verbose mode
- journalctl -o verbose

### Follow
- journalctl -f

### Last 20
- journalctl -n 20

### Kernel Level Events
- journalctl --dmesg
- journalctl -k

### View man page
- man journalctl
- journalctl --help


### View logs of a specific service
- journalctl -u ssh

### View logs only from the current boot
- journalctl -b

### View logs filtered by date or time
- journalctl --since yesterday --until today
- journalctl --since yesterday
- journalctl --since "2024-11-01" --until "2024-11-10"
