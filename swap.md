# Ceph VM Swappiness Tuning

## 1. Check current swappiness

``` bash
cat /proc/sys/vm/swappiness
```

## 2. Temporarily set swappiness to 1

``` bash
sysctl -w vm.swappiness=1
```

## 3. Create the Ceph tuning configuration

``` bash
nano /etc/sysctl.d/99-ceph-tuning.conf
```

Add:

``` conf
vm.swappiness = 1
vm.min_free_kbytes = 1048576
```

## 4. Apply the configuration

``` bash
sysctl -p /etc/sysctl.d/99-ceph-tuning.conf
```

## 5. Verify the settings

``` bash
cat /proc/sys/vm/swappiness
sysctl vm.swappiness
sysctl vm.min_free_kbytes
```
