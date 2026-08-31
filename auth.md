# Auth

List all users:
```bash
ceph auth ls
```

Create a new user for proxmox client:
```bash
ceph auth get-or-create client.pve \
  mon 'allow *' \
  osd 'allow *' \
  --key_type aes
```

Get the key details:
```bash
ceph auth get client.pve
```

Delete the user:
```bash
ceph auth del client.pve
```


---

Create a new Admin key with legacy `aes` key type:
```bash
ceph auth get-or-create client.admin2 \
  mds 'allow *' \
  mgr 'allow *' \
  mon 'allow *' \
  osd 'allow *' \
  --key_type aes
```

---


### Ceph Backup Client

All standard users must start with `client`:
```bash
ceph auth get-or-create client.backup mon 'allow r' osd 'allow rw pool=rbd_pool'
````

```bash
ceph auth get client.backup > /root/ceph.client.backup.keyring
```

```bash
cat /root/ceph.client.backup.keyring
```

```bash
ceph auth caps client.backup mon 'allow r' osd 'allow rw pool=rbd_pool, allow rw pool=archive_pool'
```

```bash
ceph auth rm client.backup
```

```bash
ceph auth get client.backup
```


