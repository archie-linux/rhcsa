### Manage Users and Groups

### Create, delete, and modify users and groups

- useradd user
- passwd user
- groupadd group
- usermod -aG group user

### Configure superuser access

Edit /etc/sudoers or /etc/sudoers.d/*.

- sudo visudo
user ALL=(ALL:ALL) ALL
