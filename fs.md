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

