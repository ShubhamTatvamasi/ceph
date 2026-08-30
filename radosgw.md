# radosgw


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
