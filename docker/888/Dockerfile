FROM quay.io/centos/centos:stream9
run dnf -y install nfs-utils
run mkdir /sharefolder
run chmod 777 /sharefolder
run chown nobody /sharefolder
run echo "/sharefolder    *(rw,no_root_squash)" > /etc/exports
run echo -e "[nfsd]\nvers3=n" > /etc/nfs.conf 
EXPOSE 2049
VOLUME [ "/sharefolder" ]

ENTRYPOINT ["/usr/sbin/rpc.nfsd"]



# CMD ["/usr/sbin/rpc.nfsd", "--debug", "8", "--no-udp", "--no-nfs-version", "2", "--no-nfs-version", "3"]


# CMD ["nginx", "-g", "daemon off;"]

# CMD ["sh", "-c", "rpcbind && /usr/sbin/rpc.nfsd && /usr/sbin/rpc.mountd"]
# run echo -e "#!/bin/bash\nrpcbind\n/usr/sbin/rpc.nfsd 4\n/usr/sbin/rpc.mountd\n/usr/sbin/rpc.statd\n/usr/sbin/rpc.lockd\n" > /startup.sh
# run chmod 777 /startup.sh
# ENTRYPOINT ["/startup.sh"]

# ENTRYPOINT ["/usr/local/bin/nfsd", "start"]

# ENTRYPOINT ["/usr/sbin/rpc.nfsd", "8"]
# CMD ["-N", "4"]
