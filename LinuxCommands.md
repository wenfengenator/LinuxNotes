# LinuxCommands

## ECC memory check
- sudo dmidecode -t memory | grep -iE "Error Correction Type"
## NVME cli
- sudo apt install nvme-cli
- sudo nvme list
- sudo nvme smart-log /dev/nvme0n1
## Change swap size (to 20GB)
- sudo swapoff -a
- sudo dd if=/dev/zero of=/swapfile bs=20M count=1k
- sudo mkswap /swapfile
- sudo chown root:root /swapfile
- sudo chmod 0600 /swapfile
- sudo swapon /swapfile
  * After that make sure there's the following line from /etc/fstab
  * /swapfile                     none            swap    sw              0       0
