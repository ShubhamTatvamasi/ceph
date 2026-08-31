# Remove Node from cluster

Check services of a specific node:
```bash
ceph orch ps --hostname ceph-node3
```

Remove OSD from specific node:
```bash
ceph orch osd rm 1
ceph orch osd rm 5
ceph orch osd rm 8
```

Check OSD drain status:
```bash
ceph orch osd rm status
```

Remove services from node:
```bash
ceph orch daemon rm mon.ceph-node3
ceph orch daemon rm mgr.ceph-node3.yphazc
ceph orch daemon rm mds.myfs.ceph-node3.wcidyo
ceph orch daemon rm rgw.myrgw.ceph-node3.ectrwd
```

Drain host:
```bash
ceph orch host drain ceph-node3 --force
```
