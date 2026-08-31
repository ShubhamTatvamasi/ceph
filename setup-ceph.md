# Setup Ceph Cluster

Create 167 user:
```bash
sudo groupadd -g 167 ceph
sudo useradd -r \
  -u 167 \
  -g 167 \
  -d /var/lib/ceph \
  -s /usr/sbin/nologin \
  ceph
```
> All Nodes

Install cephadm:
```bash
sudo apt install -y cephadm python3-ceph-common
```
> All Nodes

Bootstrap the primary node:
```bash
sudo cephadm bootstrap \
  --mon-ip 10.10.153.255 \
  --cluster-network 10.20.0.0/16
```
> Only First Node

Add more nodes to the cluster:
```bash
ceph orch host add ceph-node2 --labels _admin
ceph orch host add ceph-node3 --labels _admin
```
