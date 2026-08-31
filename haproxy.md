# haproxy

Install `haproxy`:
```bash
sudo apt install -y haproxy
```

Backup original config file:
```bash
sudo mv /etc/haproxy/haproxy.cfg /etc/haproxy/haproxy.cfg.bak
```

Setup new config file:
```bash
sudo vim /etc/haproxy/haproxy.cfg
```

Setup `haproxy` config for s3:
```
global
    log 127.0.0.1:514 local2
    chroot /var/lib/haproxy
    maxconn 4000
    user haproxy
    group haproxy
    daemon

    stats socket /var/lib/haproxy/stats

    ssl-default-bind-ciphers PROFILE=SYSTEM
    ssl-default-server-ciphers PROFILE=SYSTEM

defaults
    mode http
    log global
    option dontlognull
    option http-server-close
    option forwardfor except 127.0.0.0/8
    option redispatch

    retries 3

    timeout http-request 10s
    timeout queue 1m
    timeout connect 10s
    timeout client 1m
    timeout server 1m
    timeout http-keep-alive 10s
    timeout check 10s

    maxconn 3000

    log-format "client=%ci:%cp frontend=%ft backend=%b server=%s status=%ST bytes=%B request=\"%r\""

frontend ceph_s3
    bind *:80
    default_backend ceph_rgw

backend ceph_rgw
    balance roundrobin

    option httpchk HEAD /
    http-check expect status 200

    server rgw1 10.10.153.255:80 check inter 3s fall 3 rise 2
    server rgw2 10.10.204.94:80 check inter 3s fall 3 rise 2
    server rgw3 10.10.169.182:80 check inter 3s fall 3 rise 2
```

Restart `haproxy`:
```bash
sudo systemctl restart haproxy
```

Check status:
```bash
sudo systemctl status haproxy
```


