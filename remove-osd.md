# Remove OSD

Mark osd out:
```bash
ceph osd out osd.7
```

Remove the OSD disk from cluster:
```bash
ceph orch osd rm 7
```

Replace the OSD disk from cluster:
```bash
ceph orch osd rm 7 --replace
```

Check status of disk:
```bash
ceph orch osd rm status
```
