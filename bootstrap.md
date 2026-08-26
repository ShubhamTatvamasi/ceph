# bootstrap


Create ceph user and group on all nodes:
```bash
groupadd -g 167 ceph
useradd -r \
  -u 167 \
  -g 167 \
  -d /var/lib/ceph \
  -s /usr/sbin/nologin \
  ceph
```

---

bootstrap cluster on node1:
```bash
sudo cephadm bootstrap \
  --mon-ip 10.10.153.255 \
  --cluster-network 10.20.0.0/16
```

Get public key from node1:
```bash
cephadm shell -- ceph cephadm get-pub-key > ceph.pub
```
