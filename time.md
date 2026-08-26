# time


All nodes should have same time synced by chrony


```bash
sudo apt install chrony
```
> On ubuntu `chrony` is pre-installed

```bash
systemctl status chronyd
```

Confirm time of all nodes:
```bash
timedatectl
```
