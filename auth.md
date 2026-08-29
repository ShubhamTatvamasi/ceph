# Auth

List all users:
```bash
ceph auth ls
```

Create a new user for proxmox client:
```bash
ceph auth get-or-create client.pve \
  mon 'allow *' \
  osd 'allow *' \
  --key_type aes
```

Get the key details:
```bash
ceph auth get client.pve
```

Delete the user:
```bash
ceph auth del client.pve
```


