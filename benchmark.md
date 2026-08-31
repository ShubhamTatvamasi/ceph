# Ceph RBD Benchmark Commands

Run RADOS benchmark:
```bash
rados bench -p rbd_pool 10 write --no-cleanup
````

Cleanup RADOS benchmark data:
```bash
run rados bench -p rbd_pool 10 cleanup
```

Create a 10 GB RBD image:
```bash
rbd create bench_image --size 10G --pool rbd_pool
```

Run RBD benchmark:
```bash
rbd bench --io-type write --io-pattern rand --io-size 4K --io-total 256MB rbd_pool/bench_image
```

