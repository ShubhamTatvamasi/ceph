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
ceph osd pool create rdb_pool
```

Enable pool deletion:
```bash
ceph config set mon mon_allow_pool_delete true
```

delete the pool:
```bash
ceph osd pool rm rdb_pool rdb_pool --yes-i-really-really-mean-it
```

