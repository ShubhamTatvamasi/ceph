# Auth

List all users:
```bash
ceph auth ls
```

Create a new user for proxmox client:
```bash
ceph auth get-or-create client.pve \
  mon 'allow *' \
  osd 'allow *'
```

Delete the user:
```bash
ceph auth del client.pve
```
