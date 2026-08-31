# radosgw-admin


List all users:
```bash
radosgw-admin user list
```

Create s3 user:
```bash
radosgw-admin user create \
  --uid=s3user \
  --display-name="My First S3 User"
```

Get user details:
```bash
radosgw-admin user info --uid=s3user
```

Delete user:
```bash
radosgw-admin user rm --uid=s3user
```

---

### Ceph S3 RGW Commands


```bash
radosgw-admin user suspend --uid=s3user
```

```bash
radosgw-admin user info --uid=s3user
```

```bash
radosgw-admin user enable --uid=s3user
```

```bash
radosgw-admin bucket list
```

---

### Policy 

```bash
cd /root
```

```bash
vim policy.json
```

policy.json
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": "*",
      "Action": ["s3:GetObject"],
      "Resource": ["arn:aws:s3:::my-first-bucket/*"]
    }
  ]
}
```

