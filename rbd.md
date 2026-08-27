# rbd



Initialize RBD pool:
```bash
rbd pool init rbd_pool
```

Create a new disk image: 
```bash
rbd create db_disk --size 10G --pool rbd_pool
```

List rbd images:
```bash
rbd ls rbd_pool
```

Check the disk details:
```bash
rbd info rbd_pool/db_disk
```

---

### Attach the disk to a VM

Map disk to device:
```bash
rbd map rbd_pool/db_disk
```

Verify:
```bash
ls /dev/rbd0
```

Create the filesystem:
```
mkfs.xfs /dev/rbd0
```

---

Remove extra map:
```bash
rbd unmap /dev/rbd1
```
