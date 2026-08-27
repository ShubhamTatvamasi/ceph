# Ceph Monitor

Check the key algo:
```bash
ceph mon dump | grep -E 'auth_allowed_ciphers|auth_preferred_cipher'
```

Enable legacy `aes` key:
```bash
ceph mon set auth_allowed_ciphers aes,aes256k
```

Enable legacy `aes` key:
```bash
ceph mon set auth_preferred_cipher aes
```

Verify keys:
```bash
ceph mon dump | grep auth_.*cipher
```

Change `auth_preferred_cipher` back to `aes256k` key once you have the new key:
```bash
ceph mon set auth_preferred_cipher aes256k
```

---

Rotate key with legacy `aes` algo:
```bash
ceph auth rotate client.admin
```

Update the key:
```
cat << EOF > /etc/ceph/ceph.keyring
[client.admin]
  key = AQASPpBq3+jTGRAA4W0yZCi7WEMC7KqG2j9JXQ==
  caps mds = "allow *"
  caps mgr = "allow *"
  caps mon = "allow *"
  caps osd = "allow *"
EOF
```

Verify new key:
```bash
ceph auth get client.admin
```



