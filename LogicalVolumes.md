### Configure Local Storage

### List, create, delete partitions
- Use lsblk, fdisk, gdisk.

### Create and remove physical volumes

- pvcreate /dev/sdb
- pvremove /dev/sdb

### Assign physical volumes to volume groups

- vgcreate vg_name /dev/sdb

### Create and delete logical volumes

- lvcreate -L 10G -n lv_name vg_name
- lvremove /dev/vg_name/lv_name

### Format the new LV

- sudo mkfs.ext4 /dev/vg_name/lv_name

### Mount the new LV

- mkdir /mnt/lv_dir
- sudo mount /dev/vg_name/lv_name /mnt/lv_dir

### Verify the chages
- df -h

### Add entries in /etc/fstab to persit the changes

- blkid /dev/vg_name/lv_name
- UUID=<lv_name-uuid> /mnt/lv_dir ext4 defaults 0 2
