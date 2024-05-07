# multidrive
Synchronize directories on multiple drives. Both local and remote.

# Motivation
A plethora of solutions exist when it comes to backup and data synchronization. The most well known open source project is perhaps Nextcloud. But syncthing and Seafile are also strong contenders.

And while all of these solutions work great, they take some effort to maintain when selfhosting them. Sure, docker and snapd exist, but whenever a database (other than sqlite) comes in, things get more difficult to backup and are less portable.

This is why `multidrive` uses a "file only" approach. Your backup / mirror is simply the same directory on another drive or network share. Using something like btrfs' snapshot feature you then turn synchronization into actual backup – meaning you not olny have a 
