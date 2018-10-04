``` shell
docker run -d --name frp-server -p 7000:7000 -v /opt/frps-config:/conf pengpan/frps-docker
```

在宿主机上，添加`frps.ini`文件到`/opt/frps-config`目录
