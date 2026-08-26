# time


All nodes should have same time synced by chrony


```bash
sudo apt install chrony
```
> On ubuntu `chrony` is pre-installed

```bash
systemctl status chronyd
```

Check the sources:
```bash
chronyc sources
```

---

Confirm time of all nodes:
```bash
timedatectl
```
