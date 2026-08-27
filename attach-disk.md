 # Attach Disk

Install dependencies:
```bash
sudo apt install -y ceph ceph-common
```

Check if ceph has been installed:
```bash
ceph --version
```

---

Copy `ceph.conf` and `ceph.client.admin.keyring` files from ceph cluster node to VM at same location

```bash
cat /etc/ceph/ceph.conf
```

```bash
sudo cat /etc/ceph/ceph.client.admin.keyring
```

```bash
sudo vim /etc/ceph/ceph.conf
sudo vim /etc/ceph/ceph.client.admin.keyring
```

All the files should be owned by root:
```bash
sudo chown root:root /etc/ceph/*
```

Validate keyring file:
```bash
sudo ceph-authtool /etc/ceph/ceph.client.admin.keyring --list
```


