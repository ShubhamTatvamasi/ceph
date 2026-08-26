# orch

Get inside the cephadm shell container
```bash
cephadm shell
```

list all hosts:
```bash
ceph orch host ls
```

Add more nodes to the cluster:
```bash
ceph orch host add ceph-node2 --labels _admin
ceph orch host add ceph-node3 --labels _admin
```
> make sure we have 167 user and group before this

Check app the node services:
```bash
ceph orch ps
```

Place both mon and mgr services on all 3 nodes:
```bash
ceph orch apply mon --placement="ceph-node1,ceph-node2,ceph-node3"
ceph orch apply mgr --placement="ceph-node1,ceph-node2,ceph-node3"
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

