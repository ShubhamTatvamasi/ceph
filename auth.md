# Auth

Create a new user for proxmox client:
```bash
ceph auth get-or-create client.pve \
  mon 'allow *' \
  osd 'allow *'
```
