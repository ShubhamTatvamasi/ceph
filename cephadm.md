# cephadm

https://docs.ceph.com/en/latest/releases/#active-releases \
https://download.ceph.com


```bash
sudo apt install -y cephadm python3-ceph-common
```

manual
```
CEPH_RELEASE=20.2.4
curl --silent --remote-name --location \
  https://download.ceph.com/rpm-${CEPH_RELEASE}/el9/noarch/cephadm
```

Add user to the docker group
```bash
sudo usermod -aG docker $USER
```

---

Add `tentacle` repo:
```bash
cephadm add-repo --release tentacle
```

