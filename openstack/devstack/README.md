# Installation of devstack on ubuntu 24.04

```
useradd -s /bin/bash -d /opt/stack -m stack
chmod +x /opt/stack
echo "stack ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers
```

```
su - stack
git clone --depth=1 -b stable/2024.2 https://github.com/openstack/devstack.git
cd devstack
```

```
cat << EOF > local.conf
[[local|localrc]]
ADMIN_PASSWORD=admindev
DATABASE_PASSWORD=databasedev
RABBIT_PASSWORD=rabbitdev
SERVICE_PASSWORD=servicedev
HOST_IP=192.168.220.120
EOF
```

```
./stack.sh
```

## Installation Requirements
### VMware Workstation Download Link
https://s3.ir-thr-at1.arvanstorage.ir/astek-packages/VMware-workstation-full-17.6.0-24238078.exe   

### 
https://s3.ir-thr-at1.arvanstorage.ir/astek-packages/Openstack.zip