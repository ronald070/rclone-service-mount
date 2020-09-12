# rclone-service-mount
This is a script to mount rclone as a service on your [CentOS](https://www.centos.org/) 6 server.

# Before you use this script
Before yuo can use this script you need to configure [rclone](https://rclone.org) first and you need to create an remote location in rclone. Also see [rclone install documentation](https://rclone.org/install/).
# Installation
After downloading you need to change the script. 

## Change the following variables 

    rclone_remote="Archive:"
    mount_dir="/cloud/Archive"
    log_file="/var/log/rclone"

## Copy the files
You need to copy rclone-archive to /etc/rc.d/init.d

## Service operations
You can start, stop or get status of the service.

### Start rclone-archive
    service rclone-archive start

### Stop rclone-archive
    service rclone-archive stop

### Status rclone-archive
    service rclone-archive status

### Install at boot
    chkconfig --add rclone-archivbe


