# Ceph CLI

Check cluster status:
```bash
ceph status
```

### OSD

Check the status of disks:
```bash
ceph osd status
```

Check the tree of disks:
```bash
ceph osd tree
```

Mark OSD which you want to take out:
```bash
ceph osd out 3
```

Check if there is any data on the disk:
```bash
ceph osd df tree
```

Add the disk back again:
```bash
ceph osd in 3
```
