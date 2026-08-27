# sudoers

Edit ceph sudoers file:
```bash
sudo EDITOR=vim visudo -f /etc/sudoers.d/ceph-smartctl
```

Update this value:
```
ceph ALL=(root) NOPASSWD: /usr/sbin/smartctl
ceph ALL=(root) NOPASSWD: /usr/sbin/nvme
```

Validate:
```bash
sudo visudo -cf /etc/sudoers.d/ceph-smartctl
```
