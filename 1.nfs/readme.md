## NFS Server

1. sudo apt update
2. sudo apt install nfs-kernel-server
3. sudo mkdir -p /mnt/nfs_share
4. sudo chown -R nobody:nogroup /mnt/nfs_share/
5. sudo chmod 777 /mnt/nfs_share/
6. echo "/mnt/nfs_share \*(rw,sync,no_subtree_check,insecure)" | sudo tee -a /etc/exports
7. sudo exportfs -a
8. sudo systemctl restart nfs-kernel-server

## NFS Client (Ubuntu)

1. sudo apt update
2. sudo apt install nfs-common
3. sudo mkdir -p /mnt/nfs_clientshare
4. sudo mount 172.27.22.64:/mnt/nfs_share1 /mnt/nfs_clientshare1
5. ls -l /mnt/nfs_clientshare/

######worker-node
***If we add any worker node you should install below command

1. sudo apt update
2. sudo apt install nfs-common


## NFS Client (MacOS)

1. mkdir nfs_clientshare
2. sudo mount -o nolocks -t nfs <IP>:/mnt/nfs_share ./nfs_clientshare
