# erasure coding

List erasure coding profiles:
```bash
ceph osd erasure-code-profile ls
```

Get the profile details:
```bash
ceph osd erasure-code-profile get default
```

Create a new profile:
```bash
ceph osd erasure-code-profile set erasure-k4-m2 k=4 m=2
```

Check the details of erasure-k4-m2 profile:
```bash
ceph osd erasure-code-profile get erasure-k4-m2
```

