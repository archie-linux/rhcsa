### List types

systemctl --type=service
systemctl list-unit-files --type=service

### Boot, reboot, and shut down a system normally

- systemctl reboot
- systemctl poweroff

### Boot systems into different targets manually

- systemctl isolate multi-user.target

### Start, stop, and check the status of network services

- systemctl stop sshd
- systemctl start sshd
- systemctl status sshd
