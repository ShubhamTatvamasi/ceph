# aws

Install `aws` cli:
```bash
sudo apt install -y awscli
```

---

Setup directory:
```
mkdir -p ~/.aws
```

Setup credentials
```
cat << EOF > ~/.aws/credentials
[default]
aws_access_key_id = HWQAPPQPAYFXSY601HMB
aws_secret_access_key = U9M7zcw7DeMN4NYR5FdXN4RgE4KkRce0mUJ0fL6W
EOF
```

Setup config
```
cat << EOF > ~/.aws/config
[default]
region = us-east-1
endpoint_url = http://10.10.153.255
EOF
```


