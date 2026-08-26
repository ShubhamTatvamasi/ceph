# orch

list all hosts:
```bash
ceph orch host ls
```

Add more nodes to the cluster:
```bash
cephadm shell -- ceph orch host add ceph-node2 --labels _admin
cephadm shell -- ceph orch host add ceph-node3 --labels _admin
```

```bash
cephadm shell -- ceph orch host ls
```

