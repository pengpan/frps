# frps
Document: [https://github.com/fatedier/frp/blob/master/README.md](https://github.com/fatedier/frp/blob/master/README.md)

# how to use
```
$ mkdir /opt/frps/config

$ cat > /opt/frps/config/frps.ini << EOF
# frps.ini
[common]
bind_port = 7000

vhost_http_port = 80
vhost_https_port = 443

dashboard_port = 7500
# dashboard's username and password are both optional，if not set, default is admin.
dashboard_user = admin
dashboard_pwd = admin
EOF

$ docker run --name frp-server --restart=always \
-p 6000:6000 \
-p 7000:7000 \
-p 8305:7500 \
-p 8306:80 \
-p 8307:443 \
-v /opt/frps/config:/conf -d pengpan/frps
```
