# fs

Create `cephfs.myfs.meta` and `cephfs.myfs.data` pools:
```bash
ceph fs volume create myfs
```

List pools:
```bash
ceph osd lspools
```

Check status, we will be having more `pgs`:
```bash
ceph -s
```

Check status for filesystem:
```bash
ceph fs status
```

---

Create `client.fsuser`:
```bash
ceph fs authorize myfs client.fsuser / rw
```

---

Update file on node:
```bash
vim /etc/ceph/ceph.client.fsuser.keyring
```

```
chmod 600 /etc/ceph/ceph.client.fsuser.keyring
```

```bash
mkdir -p /mnt/shared_data
```

Mount the file system:
```bash
mount -t ceph 10.10.153.255,10.10.204.94,10.10.169.182:/ /mnt/shared_data -o name=fsuser
```

Check the mounted path:
```bash
df -h
```

---

```bash
vim /etc/fstab
```

```
10.10.153.255,10.10.204.94,10.10.169.182:/ /mnt/shared_data ceph
name=fsuser,secretfile=/etc/ceph/fsuser.secret,netdev 0 0
```




