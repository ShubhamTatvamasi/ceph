# Placement Groups

List pg status:
```bash
ceph pg stat
```

Dump all PG details
```bash
ceph pg dump
```

Get the details of a pg:
```bash
ceph pg 1.0 query
```

Check the total number of placement groups we have for `rbd_pool` pool:
```bash
ceph osd pool get rbd_pool pg_num
```

List by pool:
```bash
ceph pg ls-by-pool rbd_pool
```

List by OSD:
```bash
ceph pg ls-by-osd 0
```
