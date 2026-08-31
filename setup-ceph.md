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

Install cephadm:
```bash
sudo apt install -y cephadm python3-ceph-common
```

Bootstrap the primary node:
```bash
sudo cephadm bootstrap \
  --mon-ip 10.10.153.255 \
  --cluster-network 10.20.0.0/16
```

Install Ceph Cluster:
```bash
sudo cephadm install
```
