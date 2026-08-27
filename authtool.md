# authtool

Generate new key:
```bash
ceph-authtool \
  --gen-key \
  --create-keyring /tmp/ceph.client.test.keyring \
  -n client.test
```

