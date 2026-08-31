# Ceph Health

Check cluster status:
```bash
ceph status
```

Check ceph health status:
```bash
ceph health detail
```

Mute OSD down alert:
```bash
ceph health mute OSD_DOWN 1h
```

Unmute OSD down alert:
```
ceph health unmute OSD_DOWN
```


---

Mute AES Key warning:
```bash
ceph health mute AUTH_INSECURE_CLIENT_KEY_TYPE
ceph health mute AUTH_INSECURE_KEYS_ALLOWED
ceph health mute AUTH_INSECURE_KEYS_CREATABLE
```
