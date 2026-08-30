# rados

Create a find me file:
```bash
echo "I am hunting for this file!" > find_me.txt
```

Upload file as raw object: 
```bash
rados put my_raw_object find_me.txt -p rbd_pool
```
