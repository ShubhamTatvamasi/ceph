# pool

List all pools:
```bash
ceph osd pool ls
```

List all pools with details:
```bash
ceph osd pool ls detail
```

Create a new pool
```bash
ceph osd pool create rbd_pool
```

Change replica to 4:
```bash
ceph osd pool set rbd_pool size 4
```

Enable pool deletion:
```bash
ceph config set mon mon_allow_pool_delete true
```

delete the pool:
```bash
ceph osd pool rm rbd_pool rbd_pool --yes-i-really-really-mean-it
```

