# crush



list all crush rules:
```bash
ceph osd crush rule ls
```

Give the rule details:
```bash
ceph osd crush rule dump
```

---


Remove device class:
```
ceph osd crush rm-device-class osd.0
```

Set device class:
```
ceph osd crush set-device-class nvme osd.0
```

