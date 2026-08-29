# cephadm

https://docs.ceph.com/en/latest/releases/#active-releases \
https://download.ceph.com


Access the ceph shell:
```bash
sudo cephadm shell
```

---

Install cephadm:
```bash
sudo apt install -y cephadm python3-ceph-common
```

Install ceph
```bash
sudo cephadm install
```

---

Add user to the docker group
```bash
sudo usermod -aG docker $USER
```

---

manual
```
CEPH_RELEASE=20.2.4
curl --silent --remote-name --location \
  https://download.ceph.com/rpm-${CEPH_RELEASE}/el9/noarch/cephadm
```

Add `tentacle` repo:
```bash
sudo cephadm add-repo --release tentacle
```

---

```
dpkg-query -W cephadm
```




