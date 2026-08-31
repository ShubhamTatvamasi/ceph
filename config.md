# config

Get the memory target:
```
ceph config get osd osd_memory_target
```

Set the memory target:
```
ceph config set osd osd_memory_target 8G
```

Remove custom value of the memory target:
```
ceph config rm osd osd_memory_target
```

Get the memory target autotune is enabled or not:
```bash
ceph config get osd osd_memory_target_autotune
```
