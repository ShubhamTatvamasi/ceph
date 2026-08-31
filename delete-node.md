# Remove Node from cluster

Check services of a specific node:
```bash
ceph orch ps --hostname ceph-node3
```

Format disks:
```bash
ceph orch device zap ceph-node3 /dev/sdb --force
ceph orch device zap ceph-node3 /dev/sdc --force
ceph orch device zap ceph-node3 /dev/sdd --force
```

Remove OSD from specific node:
```bash
ceph orch osd rm 1
ceph orch osd rm 5
ceph orch osd rm 8
```

Prune disks:
```bash
ceph osd purge 1 --yes-i-really-mean-it
ceph osd purge 5 --yes-i-really-mean-it
ceph osd purge 8 --yes-i-really-mean-it
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

Remove node from cluster:
```bash
ceph orch host rm ceph-node3 --offline --force
```

