# Ceph Manager Dashboard

Get ceph manager URL:
```bash
ceph mgr services
```

Check stats:
```bash
ceph mgr stat
```

Remove the mgr daemon from the node:
```bash
ceph orch daemon rm mgr.ceph-node3.mdjexh
```

Add the daemon back again:
```bash
ceph orch daemon add mgr ceph-node3
```
