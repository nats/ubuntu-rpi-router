# ubuntu-rpi-router
This repository contains the cloud-init files I use to configure a Raspberry Pi as my home router.

# Requirements
- Raspberry Pi with Ubuntu image installed
- A second ethernet port (either a USB to Ethernet adapter, or a CM4 kit with additional port)

# Instructions
1. Flash SD card / eMMC with Ubuntu image
2. Once flash is complete (and before getting Raspberry Pi ready to boot), check the SD card / eMMC for partitions: there should be a small FAT32 partition and a larger EXT4 one
3. Copy `meta-data`, `user-data`, and `network-config` from this repository into the FAT32 partition, overwriting the existing files of the same name.
4. Boot the Raspberry Pi.
5. Once boot finished, SSH to `root@192.168.10.1` with public key.
