# Ceph VM Swappiness Tuning

Check current swappiness
``` bash
cat /proc/sys/vm/swappiness
```

Temporarily set swappiness to 1
``` bash
sysctl -w vm.swappiness=1
```

Create the Ceph tuning configuration
``` bash
vim /etc/sysctl.d/99-ceph-tuning.conf
```

Add:
``` conf
vm.swappiness = 1
vm.min_free_kbytes = 1048576
```

Apply the configuration
``` bash
sysctl -p /etc/sysctl.d/99-ceph-tuning.conf
```

Verify the settings
``` bash
cat /proc/sys/vm/swappiness
sysctl vm.swappiness
sysctl vm.min_free_kbytes
```
