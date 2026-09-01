# Ceph crash

Check crashes:
```bash
ceph crash ls
```

Get details of crash:
```bash
ceph crash info <crash-id>
```

---

Simulate Crash

Check if we can stop OSD daemon:
```bash
osd ok-to-stop 7
```

Stop OSD Daemon:
```bash
ceph orch daemon stop osd.7
```

Start OSD again:
```bash
ceph orch daemon start osd.7
```

Verify:
```bash
ceph osd tree
```

---

```bash
systemctl status ceph-crash
```

```
systemctl restart ceph-crash
```
