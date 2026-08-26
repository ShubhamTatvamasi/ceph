# Ceph OSD

Check the status of disks:
```bash
ceph osd status
```

Check the tree of disks:
```bash
ceph osd tree
```

---

Mark OSD which you want to take out:
```bash
ceph osd out 3
```

Delete OSD disk from ceph cluster:
```bash
ceph osd purge 3
```

Check if there is any data on the disk:
```bash
ceph osd df tree
```

Add the disk back again:
```bash
ceph osd in 3
```

---

Remove device class:
```
ceph osd crush rm-device-class osd.0
```

Set device class:
```
ceph osd crush set-device-class nvme osd.0
```

---

List all pools:
```bash
ceph osd pool ls
```

Create a new pool
```bash
ceph osd pool create repool1
```

delete the pool:
```bash
ceph osd pool rm repool1
```





