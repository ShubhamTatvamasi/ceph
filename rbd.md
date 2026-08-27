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
