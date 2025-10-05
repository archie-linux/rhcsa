### Manage Networking

### Configure IP addresses
- Use nmcli, nmtui.

### Configure Static IP

- nmcli connection show
- nmcli connection modify enp0s1 ipv4.addresses 192.168.2.100/24
- nmcli connection modify enp0s1 ipv4.gateway 192.168.2.1
- nmcli connection modify enp0s1 ipv4.dns 8.8.8.8
- nmcli connection modify enp0s1 +ipv4.routes "192.168.64.0/24 192.168.2.1"
- nmcli connection modify enp0s1 ipv4.method manual
- nmcli connection down enp0s1
- nmcli connection up enp0s1

### Configure static routes:

- nmcli connection modify enp0s1 +ipv4.routes "192.168.1.0/24 192.168.2.1"
- nmcli connection up enp0s1

Verify with ip route.

- ip route

### Configure with DHCP

- nmcli connection modify enp0s1 ipv4.method auto
- nmcli connection up enp0s3

### Configure hostname resolution

### Edit /etc/hosts or /etc/resolv.conf.

- vi /etc/hosts

10.10.10.1 test.lab

- vi /etc/resolve.conf

nameserver 8.8.8.8

### Restrict network access

- firewall-cmd --add-port=22/tcp --permanent
- firewall-cmd --reload
