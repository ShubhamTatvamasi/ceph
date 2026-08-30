# rados

Create a find me file:
```bash
echo "I am hunting for this file!" > find_me.txt
```

Upload file as raw object: 
```bash
rados put my_raw_object find_me.txt -p rbd_pool
```

List all object in rbd_pool:
```bash
rados ls -p rbd_pool
```

Recover file:
```bash
rados get my_raw_object recovered_file.txt -p rbd_pool
```
