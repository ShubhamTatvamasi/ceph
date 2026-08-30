# s3fs

Install `s3fs` package:
```bash
sudo apt install -y s3fs
```

Become root:
```bash
sudo -i
```

```bash
echo "HWQAPPQPAYFXSY601HMB:U9M7zcw7DeMN4NYR5FdXN4RgE4KkRce0mUJ0fL6W" > /etc/passwd-s3fs
```

```
chmod 600 /etc/passwd-s3fs
```

```
mkdir /mnt/s3-bucket
```

Mount s3 bucket to file system:
```bash
s3fs my-first-bucket /mnt/s3-bucket \
  -o passwd_file=/etc/passwd-s3fs \
  -o url=http://10.10.153.255 \
  -o use_path_request_style
```
