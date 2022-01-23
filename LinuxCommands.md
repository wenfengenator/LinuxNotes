# LinuxCommands

## ECC memory check
- sudo dmidecode -t memory | grep -iE "Error Correction Type"
## NVME cli
- sudo apt install nvme-cli
- sudo nvme list
- sudo nvme smart-log /dev/nvme0n1
