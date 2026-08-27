# authtool

Generate new key:
```bash
ceph-authtool \
  --gen-key \
  --create-keyring /tmp/ceph.client.test.keyring \
  -n client.test
```

Verify key:
```bash
ceph-authtool \
  /tmp/ceph.client.test.keyring \
  --list
```
