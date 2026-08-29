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


Remove the device class from OSD:
```
ceph osd crush rm-device-class osd.0
```

Set `nvme` device class to an OSD:
```
ceph osd crush set-device-class nvme osd.0
```

