# Ceph Monitor

Check the key algo:
```bash
ceph mon dump | grep -E 'auth_allowed_ciphers|auth_preferred_cipher'
```

Enable legacy `aes` key:
```bash
ceph mon set auth_allowed_ciphers aes,aes256k
```

Verify keys:
```bash
ceph mon dump | grep auth_.*cipher
```
