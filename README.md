# frps
Document: [https://github.com/fatedier/frp/blob/master/README.md](https://github.com/fatedier/frp/blob/master/README.md)

# use
```
$ mkdir /opt/frps/config
$ touch /opt/frps/config/frps.ini

$ docker run -d --name frp-server -p 7000:7000 -p 8305:7500 -p 8306:80 -p 8443:443 -v /opt/frps/config:/conf pengpan/frps
```
