# crush



list all crush rules:
```bash
ceph osd crush rule ls
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

