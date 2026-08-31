# upgrade

Check current version:
```bash
ceph version
```

Check upgrade versions:
```bash
ceph orch upgrade ls
```

Check if upgrade details:
```bash
ceph orch upgrade check --image quay.io/ceph/ceph:v21.1.0
```

Start the upgrade:
```bash
ceph orch upgrade start --image quay.io/ceph/ceph:v21.1.0
```

Check upgrade status:
```bash
ceph orch upgrade status
```

Watch upgrade:
```bash
watch -n 10 ceph orch upgrade status
```

Resume upgrade:
```bash
ceph orch upgrade resume
```
