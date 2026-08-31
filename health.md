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
