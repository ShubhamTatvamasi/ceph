# orch

list all hosts:
```bash
ceph orch host ls
```

list all the services running:
```bash
ceph orch ls
```

Add more nodes to the cluster:
```bash
ceph orch host add ceph-node2 --labels _admin
ceph orch host add ceph-node3 --labels _admin
```
> make sure we have 167 user and group before this on all nodes

Check app the node services:
```bash
ceph orch ps
```

---

Place `mon` services on all 3 nodes:
```bash
ceph orch apply mon \
  --placement="ceph-node1,ceph-node2,ceph-node3"
```

Place `mgr` services on all 3 nodes:
```bash
ceph orch apply mgr \
  --placement="ceph-node1,ceph-node2,ceph-node3"
```

Place `mds` services as `myfs` on all 3 nodes:
```bash
ceph orch apply mds myfs \
  --placement="ceph-node1,ceph-node2,ceph-node3"
```

Place `rgw` services as `myrgw` on all 3 nodes:
```bash
ceph orch apply rgw myrgw \
  --placement="ceph-node1,ceph-node2,ceph-node3"
```

---

List all OSD drives:
```bash
ceph orch device ls
```

Add all OSD to the cluster:
```bash
ceph orch apply osd --all-available-devices
```


---


Format the disk if it's not available:
```bash
ceph orch device zap ceph-node2 /dev/sdb --force
```

