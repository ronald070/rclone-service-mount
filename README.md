# rclone-service-mount
This is a script to mount rclone as a service on your [CentOS](https://www.centos.org/) 6 server.

# Before you use this script
You need to install rclone and Fuse.

## Rclone
Before yuo can use this script you need to configure [rclone](https://rclone.org) first and you need to create an remote location in rclone. Also see [rclone install documentation](https://rclone.org/install/).

## Fuse
`yum install fuse`

# Installation
After downloading you need to change the script. 

## Change the following variables 

    `rclone_remote="Archive:"`
    `mount_dir="/cloud/Archive"`
    `log_file="/var/log/rclone"`

Variable      | Value
------------- | -----
rclone_remote | This is the name of the remote location that you have configured in rclone.
mount_dir     | This is the directory that is going to be the mount point.
log_file      | This is the log file that is created by the service.


## Copy the files
You need to copy rclone-service-mount to /etc/rc.d/init.

## Service operations
You can start, stop or get status of the service.

### Start rclone-archive
    service rclone-service-mount start

### Stop rclone-archive
    service rclone-service-mount stop

### Status rclone-archive
    service rclone-service-mount status

### Install at boot
    chkconfig --add rclone-service-mount


