# portainer

安装

```

docker pull portainer/portainer

```

启动

```

docker run -d -p 9000:9000 -p 8000:8000 --restart always -v /var/run/docker.sock:/var/run/docker.sock --name portainer portainer/portainer

```





